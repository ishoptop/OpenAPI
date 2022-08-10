# 公有插件的OAuth验证

{% hint style="info" %}
公共插件必须使用OAuth 2.0规范进行身份验证，才能使用Shoptop的API资源
{% endhint %}

### **术语**

在详细了解授权过程的详细信息之前，请确保您熟悉本文档中使用的一些关键术语：

| 名称  | 描述                                            |
| --- | --------------------------------------------- |
| 插件  | 与平台对接的任何应用统称为插件。                              |
| 客户端 | 想要访问商家数据的任何插件。                                |
| API | Shoptop提供的 API，客户端 可以使用 API 读取和修改店铺数据。        |
| 用户  | Shoptop 的账户持有人，通常是商家。用户 授权 客户端 通过 API 访问店铺数据。 |

### **OAuth流程**

Shoptop使用OAuth 2.0的授权代码授予流程代表用户发放访问令牌。

1. 用户请求安装该插件
2. 该插件重定向到Shoptop并加载OAuth授权页面和插件的访问范围
3. 用户同意授权并重定向至插件的redirect\_uri
4. 插件发送包括client\_id、client\_secret和code的请求到Shoptop
5. Shoptop返回携带token的响应
6. 该插件使用token向Shoptop发出API请求
7. Shoptop返回请求的数据

**第一步：获取客户端凭据**

您需要获得`Client ID`和`Client Secret`，以便在授权过程中用于表明您的身份。 获取客户端资格：请联系Shoptop的开发以获取`Client ID`和`Client Secret`，在这个过程中，你需要提供App的基本信息以及两个接口的地址（OAuth触发接口app\_uri和OAuth回调接redirect\_uri)

**第二步：请求获得许可**

已登录平台的商家在应用市场点击安装您的插件时，Shoptop会首先以Get方式调用您提供的触发接口app\_uri，app\_uri接口需要跳转至以下地址进行授权：

```
 https://{store_domain}/admin/oauth/authorize?clientId={clientId}&scope={scopes}&redirectUri={redirectUri}&responseType={responseType}
```

* **store\_domain**：店铺名称，通常是店家域名的slug
* **clientId**：应用的API密钥
* **scope**：空格分隔的scope列表替换它。 例如，要编写订单和读取顾客信息，请使用`scope=write_order read_customer`(scope之间以空格分开,查看全部scope列表)
* **redirectUri**： 您在授权客户端后重定向到应用的URL
* **responseType**：此请求下的值为code

**第三步：确认授权**

当用户单击提示中的"授权"按钮时，它们将被重定向到上面指定的客户端地址。重定向中传递的参数。

```
 http://example.com/some/redirectUri?code={authorizationCode}&shop={store_domain}&hmac={hmac}
```

在继续接下来的流程之前，请确保您的插件执行了以下安全检查。 如果检查失败，您的插件须拒绝该请求并返回错误

* 校验hmac字段，确认其值正确(Hmac生成算法)
* 该hmac是有效的。HMAC由Shoptop签名
* 该shop参数是有效的主机名，如store.ishoptop.com

如果所有安全检查均通过，则可以通过向商店的access\_token端点发送请求，用授权 code 交换为一个维持时间一年的access\_token和不过期的refresh\_token

```
 POST https://{store_domain}/api/org/oauth/token
```

该请求需要包含如下所示参数

* **clientId**：插件的客户端ID
* **clientSecret**：插件的客户端安全密钥
* **code**：回调地址中提供的授权code
* **grantType**：授权方式，该请求下的值为authorization\_code
* **redirectUri**：应用的回调地址

请求成功后的返回值：

```json
{
    "tokenType": "Bearer",
    "expiresAt": 1550546245,
    "accessToken": "eyJ0eXAiOiJKV1QiLCJh",
    "refreshToken": "def502003d28ba08a964e",
    "shopId": "2",
    "shopName": "xiong1889"
}
```

* **tokenType**：返回Bearer
* **expiresAt**：访问密钥过期时间
* **accessToken**：访问密钥
* **refreshToken**：更新密钥，用于更新密钥
* **shopId**：店铺id
* **shopName**：用户名，通常是店家域名

access\_token 失效之后，请使用下面的请求完成更新access\_token的操作（您必须保存更新之后的refresh\_token以方便再次进行更新）

```
 POST https://{store_domain}/api/org/oauth/refreshToken
```

该请求需要包含如下所示参数

* **clientId**：插件的 API key
* **clientSecret**：插件的 API secret key
* **refreshToken**: 保存在您插件中的refresh\_token值
* **grantType**：授权方式，该请求下的值为refresh\_token
* **redirectUri**：插件的回调地址

**第四步：调用 API**

客户端获得API访问token后，便可以向RESTful API发出经过身份验证的请求。这些请求 Headers 必须带有 Access-Token: {access\_token}

请求商品数据示例如下：

```
curl --request GET \
     --url https://{store_domain}/openapi/v1/orders \
     --header 'Content-Type: application/x-www-form-urlencoded;charset=utf-8' \
     --header 'Access-Token: B_x-_5aVeXNwI-4AB98s5xLIvgv0fNzGf_MuTpqtIBA'
```


# 店铺信息

**URL:** /openapi/v1/shop/

**Type:** GET

**Content-Type:** application/x-www-form-urlencoded;charset=utf-8

**Description:** 店铺信息

**Request-example:**

```
curl -X GET -i /openapi/v1/shop/
```

**Response-fields:**

| Field                | Type   | Description        | Since |
| -------------------- | ------ | ------------------ | ----- |
| code                 | number | code               | v1    |
| errorCode            | number | errorCode          | v1    |
| msg                  | string | message            | v1    |
| data                 | object | data               | v1    |
| └─shopId             | number | 店铺id               | v1    |
| └─shopName           | string | 店铺名称               | v1    |
| └─shopUrl            | string | 店铺URL              | v1    |
| └─shopFavicon        | string | 店铺favicon          | v1    |
| └─shopEmail          | string | 店主邮箱               | v1    |
| └─shopServiceEmail   | string | 服务邮箱(客服)           | v1    |
| └─shopFinancialEmail | string | 财务邮箱               | v1    |
| └─shopContactEmail   | string | 联系邮箱               | v1    |
| └─shopCurrency       | string | 币种                 | v1    |
| └─shopUtc            | string | 时区                 | v1    |
| └─shopLanguage       | string | 语言                 | v1    |
| └─utcHour            | double | 小时数                | v1    |
| └─countryCode        | string | 国家代码               | v1    |
| └─provinceCode       | string | 省份代码               | v1    |
| └─city               | string | 城市                 | v1    |
| └─address            | string | 地址                 | v1    |
| └─phone              | string | 电话                 | v1    |
| └─zip                | string | 邮编                 | v1    |
| └─moneyFormat        | string | 货币格式               | v1    |
| └─orderPrefix        | string | 订单前缀               | v1    |
| └─symbol             | string | 货币符号               | v1    |
| └─symbolLeft         | string | 货币符号左              | v1    |
| └─symbolRight        | string | 货币符号右              | v1    |
| └─beginTime          | string | 开始日期               | v1    |
| └─endTime            | string | 结束日期               | v1    |
| └─createTime         | string | 创建时间               | v1    |
| └─updateTime         | string | 更新時間               | v1    |
| └─symbolStatus       | number | 币种状态,0:可修改,1:不可以修改 | v1    |

**Response-example:**

```json
{
    "code": 0,
    "errorCode": 0,
    "msg": "请求成功",
    "data": {
        "shopId": 48,
        "shopName": "Johnny_Store",
        "shopUrl": "johnny110.testgoshoptop.com",
        "shopFavicon": "https://mall-hk.oss-cn-hongkong.aliyuncs.com/file/jpeg/2020/12/10/1336990579871547394.jpeg",
        "shopEmail": "779482518@qq.com",
        "shopServiceEmail": "779482518@qq.com",
        "shopFinancialEmail": "779482518@qq.com",
        "shopContactEmail": null,
        "shopCurrency": "CAD",
        "shopUtc": "+0800",
        "shopLanguage": "en_US",
        "utcHour": 0.0,
        "countryCode": null,
        "provinceCode": null,
        "city": null,
        "address": null,
        "phone": null,
        "zip": null,
        "moneyFormat": null,
        "orderPrefix": null,
        "symbol": "Can.＄",
        "symbolLeft": "Can.＄",
        "symbolRight": "",
        "beginTime": null,
        "endTime": null,
        "createTime": "2020-12-04 10:12:42",
        "updateTime": "2021-03-15 16:20:17",
        "symbolStatus": 1
    }
}
```

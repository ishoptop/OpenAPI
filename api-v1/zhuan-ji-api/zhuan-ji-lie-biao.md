# 专辑列表

**URL:** /openapi/v1/collections/

**Type:** GET

**Content-Type:** application/x-www-form-urlencoded;charset=utf-8

**Description:** 专辑列表

**Query-parameters:**

| Parameter | Type   | Description                      | Required | Since |
| --------- | ------ | -------------------------------- | -------- | ----- |
| pageNo    | number | 页码，从1开始                          | true     | v1    |
| pageSize  | number | 每页显示条数 default: 10, maximum: 200 | true     | v1    |
| keyword   | string | 搜索关键词                            | false    | v1    |
| shopId    | number | 店铺id                             | false    | v1    |

**Request-example:**

```
curl -X GET -i /openapi/v1/collections/?keyword=cou2q7&shopId=150&pageSize=10&pageNo=161
```

**Response-fields:**

| Field                   | Type   | Description | Since |
| ----------------------- | ------ | ----------- | ----- |
| code                    | number | code        | v1    |
| errorCode               | number | errorCode   | v1    |
| msg                     | string | message     | v1    |
| data                    | array  | data        | v1    |
| └─collectionId          | number | 专辑ID        | v1    |
| └─shopId                | number | 店铺id        | v1    |
| └─seoTitle              | string | seo标题       | v1    |
| └─seoKeywords           | string | seo关键词      | v1    |
| └─seoDescription        | string | seo描述       | v1    |
| └─handle                | string | 商品url尾缀     | v1    |
| └─collectionDescription | string | 描述          | v1    |
| └─collectionTitle       | string | 标题          | v1    |
| └─image                 | object | 专辑封面图片      | v1    |
|      └─fileRepositoryId | number | 图片文件id      | v1    |
|      └─path             | string | 图片位置        | v1    |
|      └─url              | string | 图片url       | v1    |
|      └─height           | number | 高度          | v1    |
|      └─width            | number | 宽度          | v1    |
|      └─type             | string | 文件格式类型      | v1    |
| └─sortOrder             | string | 专辑中商品的排序规则  | v1    |
| └─createTime            | string | 创建时间        | v1    |
| └─updateTime            | string | 修改时间        | v1    |
| └─spuIds                | array  | 商品专辑中的商品id  | v1    |

**Response-example:**

```json
{
    "code": 0,
    "errorCode": 0,
    "msg": "请求成功",
    "data": [
        {
            "collectionId": "1341305767802273794",
            "shopId": 48,
            "seoTitle": "苏格拉没有底",
            "seoKeywords": "",
            "seoDescription": "",
            "handle": "苏格拉没有底",
            "collectionDescription": "",
            "collectionTitle": "苏格拉没有底",
            "image": {
                "fileRepositoryId": "1339860432684871681",
                "path": "1339860432684871681.png",
                "url": "https://dev-cdn-shoptop-com.oss-cn-shanghai.aliyuncs.com/file/png/2020/12/18/1339860432684871681.png",
                "height": 48,
                "width": 48,
                "type": "image/png"
            },
            "sortOrder": "{\"sortBy\":\"sale_num\",\"sortDirection\":\"descend\"}",
            "createTime": "2020-12-22 16:53:10",
            "updateTime": "2021-03-18 10:57:30",
            "spuIds": null
        },
        {
            "collectionId": "1341304543304581121",
            "shopId": 48,
            "seoTitle": "想象之中",
            "seoKeywords": "",
            "seoDescription": "",
            "handle": "想象之中_f3qv",
            "collectionDescription": "",
            "collectionTitle": "想象之中",
            "image": null,
            "sortOrder": "{\"sortBy\":\"sale_num\",\"sortDirection\":\"descend\"}",
            "createTime": "2020-12-22 16:48:18",
            "updateTime": "2021-03-18 10:57:30",
            "spuIds": null
        }
    ]
}
```

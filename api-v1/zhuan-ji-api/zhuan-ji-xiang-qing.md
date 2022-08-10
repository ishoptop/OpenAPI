# 专辑详情

**URL:** /openapi/v1/collections/{collectionId}

**Type:** GET

**Content-Type:** application/x-www-form-urlencoded;charset=utf-8

**Description:** 专辑详情

**Path-parameters:**

| Parameter    | Type   | Description | Required | Since |
| ------------ | ------ | ----------- | -------- | ----- |
| collectionId | number | 专辑id        | true     | v1    |

**Request-example:**

```
curl -X GET -i /openapi/v1/collections/896
```

**Response-fields:**

| Field                   | Type   | Description                              | Since |
| ----------------------- | ------ | ---------------------------------------- | ----- |
| code                    | number | code                                     | v1    |
| errorCode               | number | errorCode                                | v1    |
| msg                     | string | message                                  | v1    |
| data                    | object | data                                     | v1    |
| └─collectionId          | number | 专辑ID                                     | v1    |
| └─shopId                | number | 店铺id                                     | v1    |
| └─seoTitle              | string | seo标题                                    | v1    |
| └─seoKeywords           | string | seo关键词                                   | v1    |
| └─seoDescription        | string | seo描述                                    | v1    |
| └─handle                | string | 商品url尾缀                                  | v1    |
| └─collectionDescription | string | 描述                                       | v1    |
| └─collectionTitle       | string | 标题                                       | v1    |
| └─image                 | object | 专辑封面图片                                   | v1    |
|      └─fileRepositoryId | number | 图片文件id                                   | v1    |
|      └─path             | string | 图片位置                                     | v1    |
|      └─url              | string | 图片url                                    | v1    |
|      └─height           | number | 高度                                       | v1    |
|      └─width            | number | 宽度                                       | v1    |
|      └─type             | string | 文件格式类型                                   | v1    |
| └─sortOrder             | object | 专辑中商品的排序规则                               | v1    |
|      └─sortBy           | string | 要根据哪个字段进行排序                              | v1    |
|      └─sortDirection    | string | 根据哪个字段排序进行升序或降序排序 升序:ascend ,降序: descend | v1    |

**Response-example:**

```json
{
    "code": 0,
    "errorCode": 0,
    "msg": "请求成功",
    "data": {
        "collectionId": "1341305767802273794",
        "shopId": 48,
        "seoTitle": "自动专辑有封面",
        "seoKeywords": "",
        "seoDescription": "",
        "handle": "自动专辑有封面",
        "collectionDescription": "",
        "collectionTitle": "自动专辑有封面",
        "image": {
            "fileRepositoryId": "1339860432684871681",
            "path": "1339860432684871681.png",
            "url": "https://dev-cdn-shoptop-com.oss-cn-shanghai.aliyuncs.com/file/png/2020/12/18/1339860432684871681.png",
            "height": 48,
            "width": 48,
            "type": "image/png"
        },
        "sortOrder": {
            "sortBy": "sale_num",
            "sortDirection": "descend"
        }
    }
}
```

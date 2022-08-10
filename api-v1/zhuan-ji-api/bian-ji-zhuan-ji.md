# 编辑专辑

**URL:** /openapi/v1/collections/

**Type:** PUT

**Content-Type:** application/json; charset=utf-8

**Description:** 编辑专辑

**Body-parameters:**

| Parameter             | Type   | Description                              | Required | Since |
| --------------------- | ------ | ---------------------------------------- | -------- | ----- |
| collectionId          | number | 专辑ID                                     | false    | v1    |
| shopId                | number | 店铺id                                     | false    | v1    |
| seoTitle              | string | seo标题                                    | false    | v1    |
| seoKeywords           | string | seo关键词                                   | false    | v1    |
| seoDescription        | string | seo描述                                    | false    | v1    |
| handle                | string | 商品url尾缀                                  | false    | v1    |
| collectionDescription | string | 描述                                       | false    | v1    |
| collectionTitle       | string | 标题                                       | false    | v1    |
| imageUrl              | string | 专辑封面图片                                   | false    | v1    |
| sortOrder             | object | 专辑中商品的排序规则                               | false    | v1    |
| └─sortBy              | string | 要根据哪个字段进行排序                              | false    | v1    |
| └─sortDirection       | string | 根据哪个字段排序进行升序或降序排序 升序:ascend ,降序: descend | false    | v1    |
| spuIds                | array  | 商品专辑中的商品id                               | false    | v1    |

**Request-example:**

```
curl -X PUT -H 'Content-Type: application/json; charset=utf-8' -i /openapi/v1/collections/ --data '{
    "collectionId": 31,
    "shopId": 920,
    "seoTitle": "6ynhnr",
    "seoKeywords": "uzsw8k",
    "seoDescription": "lvkw9j",
    "handle": "2kbuak",
    "collectionDescription": "ym0bgq",
    "collectionTitle": "ljsah0",
    "imageUrl": "https://dev-cdn-shoptop-com.oss-cn-shanghai.aliyuncs.com/file/png/1339860432684871681.png",
    "sortOrder": {
        "sortBy": "07hgep",
        "sortDirection": "rx98tz"
    },
    "spuIds": [
        91
    ]
}'
```

**Response-fields:**

| Field     | Type   | Description | Since |
| --------- | ------ | ----------- | ----- |
| code      | number | code        | v1    |
| errorCode | number | errorCode   | v1    |
| msg       | string | message     | v1    |
| data      | object | data        | v1    |
| └─status  | string | 状态          | v1    |

**Response-example:**

```json
{
    "code": 0,
    "errorCode": 0,
    "msg": "请求成功",
    "data": {
        "status": "success"
    }
}
```

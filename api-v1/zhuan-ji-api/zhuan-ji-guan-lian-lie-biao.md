# 专辑关联列表

**URL:** /openapi/v1/collects/

**Type:** GET

**Content-Type:** application/x-www-form-urlencoded;charset=utf-8

**Description:** 专辑关联列表

**Query-parameters:**

| Parameter    | Type   | Description                      | Required | Since |
| ------------ | ------ | -------------------------------- | -------- | ----- |
| pageNo       | number | 页码，从1开始                          | true     | v1    |
| pageSize     | number | 每页显示条数 default: 10, maximum: 200 | true     | v1    |
| shopId       | number | 店铺id                             | false    | v1    |
| spuId        | number | 商品id                             | false    | v1    |
| collectionId | number | 专辑id                             | false    | v1    |

**Request-example:**

```
curl -X GET -i /openapi/v1/collects/?shopId=807&spuId=2b3d272d-12b5-4133-bbb0-5e43e748c730&pageSize=10&collectionId=553&pageNo=571
```

**Response-fields:**

| Field               | Type   | Description | Since |
| ------------------- | ------ | ----------- | ----- |
| code                | number | code        | v1    |
| errorCode           | number | errorCode   | v1    |
| msg                 | string | message     | v1    |
| data                | object | data        | v1    |
| └─list              | array  | 数据          | v1    |
|      └─id           | number | 关联id        | v1    |
|      └─collectionId | number | 商品专辑id      | v1    |
|      └─spuId        | number | 商品spuID     | v1    |
| └─total             | number | 总量          | v1    |

**Response-example:**

```json
{
    "code": 0,
    "errorCode": 0,
    "msg": "请求成功",
    "data": {
        "list": [
            {
                "id": "1298904901201625089",
                "collectionId": "1298549559691182082",
                "spuId": "1298896645695639553"
            },
            {
                "id": "1298904901226790913",
                "collectionId": "1298549559691182082",
                "spuId": "1298548593864605698"
            }        
        ],
        "total": "1298"
    }
}
```

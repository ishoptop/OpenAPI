# 专辑关联数量

**URL:** /openapi/v1/collects/count

**Type:** GET

**Content-Type:** application/x-www-form-urlencoded;charset=utf-8

**Description:** 专辑关联数量

**Query-parameters:**

| Parameter    | Type   | Description | Required | Since |
| ------------ | ------ | ----------- | -------- | ----- |
| shopId       | number | 店铺id        | false    | v1    |
| spuId        | number | 商品id        | false    | v1    |
| collectionId | number | 专辑id        | false    | v1    |

**Request-example:**

```
curl -X GET -i /openapi/v1/collects/count?collectionId=83&shopId=767&spuId=2b3d272d-12b5-4133-bbb0-5e43e748c730
```

**Response-fields:**

| Field     | Type   | Description | Since |
| --------- | ------ | ----------- | ----- |
| code      | number | code        | v1    |
| errorCode | number | errorCode   | v1    |
| msg       | string | message     | v1    |
| data      | object | data        | v1    |
| └─count   | number | 数量          | v1    |

**Response-example:**

```json
{
    "code": 0,
    "errorCode": 0,
    "msg": "请求成功",
    "data": {
        "count": "1298"
    }
}
```

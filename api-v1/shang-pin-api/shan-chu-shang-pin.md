# 删除商品

**URL:** /openapi/v1/products/{spuId}

**Type:** DELETE

**Content-Type:** application/x-www-form-urlencoded;charset=utf-8

**Description:** 删除商品

**Path-parameters:**

| Parameter | Type   | Description | Required | Since |
| --------- | ------ | ----------- | -------- | ----- |
| spuId     | number | 商品id        | true     | v1    |

**Request-example:**

```
curl -X DELETE -i /openapi/v1/products/2b3d272d-12b5-4133-bbb0-5e43e748c730
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

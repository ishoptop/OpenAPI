# 删除专辑

**URL:** /openapi/v1/collections/{collectionId}

**Type:** DELETE

**Content-Type:** application/x-www-form-urlencoded;charset=utf-8

**Description:** 删除专辑

**Path-parameters:**

| Parameter    | Type   | Description | Required | Since |
| ------------ | ------ | ----------- | -------- | ----- |
| collectionId | number | 专辑id        | true     | v1    |

**Request-example:**

```
curl -X DELETE -i /openapi/v1/collections/972
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

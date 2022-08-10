# 删除WebHook

**URL:** /openapi/v1/webhooks/{id}

**Type:** DELETE

**Content-Type:** application/x-www-form-urlencoded;charset=utf-8

**Description:** 删除webhook

**Path-parameters:**

| Parameter | Type   | Description | Required | Since |
| --------- | ------ | ----------- | -------- | ----- |
| id        | number | id          | true     | v1    |

**Request-example:**

```
curl -X DELETE -i /openapi/v1/webhooks/749
```

**Response-fields:**

| Field     | Type   | Description | Since |
| --------- | ------ | ----------- | ----- |
| code      | number | code        | v1    |
| errorCode | number | errorCode   | v1    |
| msg       | string | message     | v1    |
| data      | object | data        | v1    |

**Response-example:**

```json
{
    "code": 0,
    "errorCode": 0,
    "msg": "请求成功",
    "data": {
        "status":"success"
    }
}
```

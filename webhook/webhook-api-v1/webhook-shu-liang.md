# WebHook数量

**URL:** /openapi/v1/webhooks/count

**Type:** GET

**Content-Type:** application/x-www-form-urlencoded;charset=utf-8

**Description:** webhook数量

**Request-example:**

```
curl -X GET -i /openapi/v1/webhooks/count
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
        "count": "1"
    }
}
```

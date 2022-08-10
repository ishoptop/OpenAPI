# WebHook详情

**URL:** /openapi/v1/webhooks/{id}

**Type:** GET

**Content-Type:** application/x-www-form-urlencoded;charset=utf-8

**Description:** webhook详情

**Path-parameters:**

| Parameter | Type   | Description | Required | Since |
| --------- | ------ | ----------- | -------- | ----- |
| id        | number | id          | true     | v1    |

**Request-example:**

```
curl -X GET -i /openapi/v1/webhooks/132
```

**Response-fields:**

| Field        | Type   | Description | Since |
| ------------ | ------ | ----------- | ----- |
| code         | number | code        | v1    |
| errorCode    | number | errorCode   | v1    |
| msg          | string | message     | v1    |
| data         | object | data        | v1    |
| └─id         | number | 主键ID        | v1    |
| └─address    | string | webhook通知地址 | v1    |
| └─topic      | string | 订阅事件名称      | v1    |
| └─createTime | string | 订阅时间        | v1    |
| └─updateTime | string | 更新时间        | v1    |

**Response-example:**

```json
{
    "code": 0,
    "errorCode": 0,
    "msg": "请求成功",
    "data": {
        "id": "1425707051551563777",
        "address": "http://localhost:8080/webhooks",
        "topic": "orders/create",
        "createTime": "2021-08-12 14:33:44",
        "updateTime": null
    }
}
```

# 创建WebHook

**URL:** /openapi/v1/webhooks/

**Type:** POST

**Content-Type:** application/json; charset=utf-8

**Description:** 创建webhook

**Request-headers:**

| Header       | Type   | Description | Required | Since |
| ------------ | ------ | ----------- | -------- | ----- |
| Access-Token | string | 访问token     | true     | v1    |

**Body-parameters:**

| Parameter | Type   | Description | Required | Since |
| --------- | ------ | ----------- | -------- | ----- |
| address   | string | webhook通知地址 | false    | v1    |
| topic     | string | 订阅的事件主题     | false    | v1    |

**Request-example:**

```
curl -X POST -H 'Content-Type: application/json; charset=utf-8' -H 'Access-Token' -i /openapi/v1/webhooks/ --data '{
    "address":"http://localhost:8080/webhooks",
      "topic":"orders/create"
}'
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

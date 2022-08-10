# WebHook列表

**URL:** /openapi/v1/webhooks/

**Type:** GET

**Content-Type:** application/x-www-form-urlencoded;charset=utf-8

**Description:** webhook列表

**Query-parameters:**

| Parameter       | Type   | Description                      | Required | Since |
| --------------- | ------ | -------------------------------- | -------- | ----- |
| pageNo          | number | 页码，从1开始                          | true     | v1    |
| pageSize        | number | 每页显示条数 default: 10, maximum: 200 | true     | v1    |
| id              | number | 主键ID                             | false    | v1    |
| address         | string | webhook通知地址                      | false    | v1    |
| topic           | string | 订阅事件名称                           | false    | v1    |
| createTimeBegin | string | 创建时间Begin                        | false    | v1    |
| createTimeEnd   | string | 创建时间End                          | false    | v1    |
| updateTimeBegin | string | 更新时间Begin                        | false    | v1    |
| updateTimeEnd   | string | 更新时间End                          | false    | v1    |

**Request-example:**

```
curl -X GET -i /openapi/v1/webhooks/?updateTimeEnd=2021-08-12 09:29:39&updateTimeBegin=2021-08-12 09:29:39&pageNo=903&pageSize=10&address=http://facebook.ishoptop.com&createTimeBegin=2021-08-12 09:29:39&topic=34kwex&createTimeEnd=2021-08-12 09:29:39&id=87
```

**Response-fields:**

| Field             | Type   | Description | Since |
| ----------------- | ------ | ----------- | ----- |
| code              | number | code        | v1    |
| errorCode         | number | errorCode   | v1    |
| msg               | string | message     | v1    |
| data              | object | data        | v1    |
| └─list            | array  | 数据          | v1    |
|      └─id         | number | 主键ID        | v1    |
|      └─address    | string | webhook通知地址 | v1    |
|      └─topic      | string | 订阅事件名称      | v1    |
|      └─createTime | string | 订阅时间        | v1    |
|      └─updateTime | string | 更新时间        | v1    |
| └─total           | number | 总量          | v1    |

**Response-example:**

```json
{
    "code": 0,
    "errorCode": 0,
    "msg": "请求成功",
    "data": {
        "list": [
            {
                "id": "1425707051551563777",
                "address": "http://localhost:8080/webhooks",
                "topic": "orders/create",
                "createTime": "2021-08-12 14:33:44",
                "updateTime": null
            }
        ],
        "total": "1"
    }
}
```

# 运单数量

**URL:** /openapi/v1/orders/{orderId}/fulfillments/count

**Type:** GET

**Content-Type:** application/json; charset=utf-8

**Description:** 运单数量

**Path-parameters:**

| Parameter | Type   | Description | Required | Since |
| --------- | ------ | ----------- | -------- | ----- |
| orderId   | number | 订单id        | true     | v1    |

**Body-parameters:**

| Parameter | Type   | Description                      | Required | Since |
| --------- | ------ | -------------------------------- | -------- | ----- |
| timeType  | string | 时间类型 created(创建时间)，updated(修改时间) | false    | v1    |
| startTime | string | 起始时间（yyyy-MM-dd HH:mm:ss）        | false    | v1    |
| endTime   | string | 结束时间（yyyy-MM-dd HH:mm:ss）        | false    | v1    |

**Request-example:**

```
curl -X GET -H 'Content-Type: application/json; charset=utf-8' -i /openapi/v1/orders/235/fulfillments/count --data '{
    "timeType": "f0uhbk",
    "startTime": "2021-08-12 09:29:37",
    "endTime": "2021-08-12 09:29:37"
}'
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
        "count": 131
    }
}
```

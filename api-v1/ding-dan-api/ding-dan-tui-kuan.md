# 订单退款

**URL:** /openapi/v1/orders/{id}/refund

**Type:** POST

**Content-Type:** application/x-www-form-urlencoded;charset=utf-8

**Description:** 订单退款

**Path-parameters:**

| Parameter | Type   | Description | Required | Since |
| --------- | ------ | ----------- | -------- | ----- |
| id        | number | 订单id        | true     | v1    |

**Request-example:**

```
curl -X POST -i /openapi/v1/orders/328/refund
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
    "code": 201,
    "errorCode": 688,
    "msg": "请求成功",
    "data": true
}
```

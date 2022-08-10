# 订单数量

**URL:** /openapi/v1/orders/count

**Type:** GET

**Content-Type:** application/x-www-form-urlencoded;charset=utf-8

**Description:** 订单数量

**Query-parameters:**

| Parameter         | Type   | Description                                                                                                                                      | Required | Since |
| ----------------- | ------ | ------------------------------------------------------------------------------------------------------------------------------------------------ | -------- | ----- |
| status            | string | 订单状态 opened(未完成)，placed(进行中)，finished(已完成)，cancelled(已取消)                                                                                        | false    | v1    |
| financialStatus   | string | 订单支付状态 waiting(待支付)，paying(支付中)，paid(已支付)，cancelled(已取消)，failed(失败)，refunding(退款中)，refund\_failed(退款失败)，refunded(已退款), partially\_refunded(部分退款) | false    | v1    |
| fulfillmentStatus | string | 订单物流状态 initialled(空)，waiting(待发货)，partially\_shipped(部分发货)，shipped(已发货)，partially\_finished(部分完成)，finished(已完成), cancelled(取消)                   | false    | v1    |
| timeType          | string | 时间类型 created(创建时间)，updated(修改时间)                                                                                                                 | false    | v1    |
| startTime         | string | 起始时间（yyyy-MM-dd HH:mm:ss）                                                                                                                        | false    | v1    |
| endTime           | string | 结束时间（yyyy-MM-dd HH:mm:ss）                                                                                                                        | false    | v1    |

**Request-example:**

```
curl -X GET -i /openapi/v1/orders/count?timeType=x4cpcv&financialStatus=sul8my&endTime=2021-08-12 09:29:37&fulfillmentStatus=aevb0j&status=ikjfdb&startTime=2021-08-12 09:29:37
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
        "count": "6"
    }
}
```

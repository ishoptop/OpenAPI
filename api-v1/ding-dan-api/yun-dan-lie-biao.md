# 运单列表

**URL:** /openapi/v1/orders/{orderId}/fulfillments

**Type:** GET

**Content-Type:** application/x-www-form-urlencoded;charset=utf-8

**Description:** 运单列表

**Path-parameters:**

| Parameter | Type   | Description | Required | Since |
| --------- | ------ | ----------- | -------- | ----- |
| orderId   | number | 订单id        | true     | v1    |

**Query-parameters:**

| Parameter | Type   | Description                      | Required | Since |
| --------- | ------ | -------------------------------- | -------- | ----- |
| pageNo    | number | 页码，从1开始                          | true     | v1    |
| pageSize  | number | 每页显示条数 default: 10, maximum: 200 | true     | v1    |
| timeType  | string | 时间类型 created(创建时间)，updated(修改时间) | false    | v1    |
| startTime | string | 起始时间（yyyy-MM-dd HH:mm:ss）        | false    | v1    |
| endTime   | string | 结束时间（yyyy-MM-dd HH:mm:ss）        | false    | v1    |

**Request-example:**

```
curl -X GET -i /openapi/v1/orders/439/fulfillments?startTime=2021-08-12 09:29:37&pageSize=10&timeType=hyb7os&endTime=2021-08-12 09:29:37&pageNo=334
```

**Response-fields:**

| Field                    | Type   | Description                                                 | Since |
| ------------------------ | ------ | ----------------------------------------------------------- | ----- |
| code                     | number | code                                                        | v1    |
| errorCode                | number | errorCode                                                   | v1    |
| msg                      | string | message                                                     | v1    |
| data                     | array  | data                                                        | v1    |
| └─id                     | number | id                                                          | v1    |
| └─orderId                | number | 订单id                                                        | v1    |
| └─status                 | string | 运单状态 waiting(待发货),shipped(已发货),finished(已完成),cancelled(已取消) | v1    |
| └─createdAt              | string | 创建时间                                                        | v1    |
| └─updatedAt              | string | 修改时间                                                        | v1    |
| └─trackingCompany        | string | 物流公司                                                        | v1    |
| └─trackingNumber         | string | 运单号                                                         | v1    |
| └─trackingCompanyCode    | string | 物流公司编号                                                      | v1    |
| └─lineItems              | array  | 测试                                                          | v1    |
|      └─productTitle      | string | 商品标题                                                        | v1    |
|      └─variantTitle      | string | 子商品标题                                                       | v1    |
|      └─quantity          | number | 商品数量                                                        | v1    |
|      └─note              | string | 备注                                                          | v1    |
|      └─image             | string | 商品图片                                                        | v1    |
|      └─price             | string | 商品售价                                                        | v1    |
|      └─compareAtPrice    | string | 商品原价                                                        | v1    |
|      └─total             | string | 总价                                                          | v1    |
|      └─sku               | string | sku                                                         | v1    |
|      └─weight            | string | 重量                                                          | v1    |
|      └─weightUnit        | string | 重量单位(kg, g ...)                                             | v1    |
|      └─vendor            | string | 商品供应商                                                       | v1    |
|      └─properties        | string | 商品属性                                                        | v1    |
|      └─productUrl        | string | 商品url                                                       | v1    |
|      └─productHandle     | string | 商品handle                                                    | v1    |
|      └─id                | number | id                                                          | v1    |
|      └─productId         | string | 商品id                                                        | v1    |
|      └─variantId         | string | 子商品id                                                       | v1    |
|      └─fulfillmentStatus | string | 运单状态                                                        | v1    |

**Response-example:**

```json
{
    "code": 0,
    "errorCode": 0,
    "msg": "请求成功",
    "data": [
        {
            "id": "1379403573553049602",
            "orderId": "1379399717192511490",
            "status": "finished",
            "createdAt": "2021-04-06 20:00:15",
            "updatedAt": "2021-04-06 20:00:24",
            "trackingCompany": "YD2021",
            "trackingNumber": "韵达国际",
            "trackingCompanyCode": "-1",
            "lineItems": [
                {
                    "productTitle": "测试二",
                    "variantTitle": "测试二",
                    "quantity": 1,
                    "note": null,
                    "image": "https://cdn.shoptop.com/1356392122307657729.png",
                    "price": "45.00",
                    "compareAtPrice": "90.00",
                    "total": "45.00",
                    "sku": "20201908",
                    "weight": "5.00",
                    "weightUnit": "kg",
                    "vendor": "这是测试供应商",
                    "properties": null,
                    "productUrl": null,
                    "productHandle": "测试二",
                    "id": "1379399717318340610",
                    "productId": "1379399645092483073",
                    "variantId": "1379399645126037505",
                    "fulfillmentStatus": "finished"
                }
            ]
        }
    ]
}
```

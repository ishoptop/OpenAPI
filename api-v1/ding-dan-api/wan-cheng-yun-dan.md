# 完成运单

**URL:** /openapi/v1/orders/{orderId}/fulfillments/{fulfillmentId}/complete

**Type:** POST

**Content-Type:** application/x-www-form-urlencoded;charset=utf-8

**Description:** 完成运单

**Path-parameters:**

| Parameter     | Type   | Description | Required | Since |
| ------------- | ------ | ----------- | -------- | ----- |
| orderId       | number | 订单id        | true     | v1    |
| fulfillmentId | number | 运单id        | true     | v1    |

**Request-example:**

```
curl -X POST -i /openapi/v1/orders/878/fulfillments/261/complete
```

**Response-fields:**

| Field                    | Type   | Description                                                 | Since |
| ------------------------ | ------ | ----------------------------------------------------------- | ----- |
| code                     | number | code                                                        | v1    |
| errorCode                | number | errorCode                                                   | v1    |
| msg                      | string | message                                                     | v1    |
| data                     | object | data                                                        | v1    |
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
    "data": {
        "id": "1425658127726391298",
        "orderId": "1425657742634758146",
        "status": "shipped",
        "createdAt": "2021-08-12 11:19:20",
        "updatedAt": "2021-08-12 11:19:20",
        "trackingCompany": "安得物流",
        "trackingNumber": "2113",
        "trackingCompanyCode": "annto",
        "lineItems": [
            {
                "productTitle": "测试-444400",
                "variantTitle": "测试-444400",
                "quantity": 1,
                "note": null,
                "image": "https://cdn.shoptop.com/1357301923878989826.png",
                "price": "1.00",
                "compareAtPrice": "10.00",
                "total": "1.00",
                "sku": "111",
                "weight": "1.00",
                "weightUnit": "kg",
                "vendor": null,
                "properties": null,
                "productUrl": null,
                "productHandle": "测试-4444",
                "id": "1425657744870322178",
                "productId": "1357302156562198530",
                "variantId": "1357302156591558657",
                "fulfillmentStatus": "shipped"
            }
        ]
    }
}
```

# 创建运单

**URL:** /openapi/v1/orders/{orderId}/fulfillments

**Type:** POST

**Content-Type:** application/json; charset=utf-8

**Description:** 创建运单

**Path-parameters:**

| Parameter | Type   | Description | Required | Since |
| --------- | ------ | ----------- | -------- | ----- |
| orderId   | number | 订单id        | true     | v1    |

**Body-parameters:**

| Parameter           | Type   | Description               | Required | Since |
| ------------------- | ------ | ------------------------- | -------- | ----- |
| lineItemIds         | string | id1,id2 运单包含的line Item Id | true     | v1    |
| trackingNumber      | string | 运单号                       | true     | v1    |
| trackingCompany     | string | 物流公司名称                    | true     | v1    |
| trackingCompanyCode | string | 物流公司代码                    | true     | v1    |

**Request-example:**

```
curl -X POST -H 'Content-Type: application/json; charset=utf-8' -i /openapi/v1/orders/768/fulfillments --data '{
    "lineItemIds": "wyn48o",
    "trackingNumber": "tpg0bm",
    "trackingCompany": "Shoptop",
    "trackingCompanyCode": "79665"
}'
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
}
```

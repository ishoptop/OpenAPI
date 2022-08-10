# 订单详情

**URL:** /openapi/v1/orders/{id}

**Type:** GET

**Content-Type:** application/x-www-form-urlencoded;charset=utf-8

**Description:** 订单详情

**Path-parameters:**

| Parameter | Type   | Description | Required | Since |
| --------- | ------ | ----------- | -------- | ----- |
| id        | number | 订单id        | true     | v1    |

**Request-example:**

```
curl -X GET -i /openapi/v1/orders/254
```

**Response-fields:**

| Field                         | Type   | Description                                                                                                                                               | Since |
| ----------------------------- | ------ | --------------------------------------------------------------------------------------------------------------------------------------------------------- | ----- |
| code                          | number | code                                                                                                                                                      | v1    |
| errorCode                     | number | errorCode                                                                                                                                                 | v1    |
| msg                           | string | message                                                                                                                                                   | v1    |
| data                          | object | data                                                                                                                                                      | v1    |
| └─orderNo                     | string | 订单编号                                                                                                                                                      | v1    |
| └─id                          | number | id                                                                                                                                                        | v1    |
| └─totalPrice                  | string | 总价                                                                                                                                                        | v1    |
| └─subTotal                    | string | 小计金额                                                                                                                                                      | v1    |
| └─currency                    | string | 货币类型                                                                                                                                                      | v1    |
| └─financialStatus             | string | 订单支付状态waiting(待支付)，paying(支付中)，paid(已支付)，cancelled(已取消)，failed(失败)，refunding(退款中)，refund\_failed(退款失败)，refunded(已退款)，partially\_refunded(部分退款)            | v1    |
| └─orderStatus                 | string | 订单状态 opened(未完成)，placed(进行中)，finished(已完成)，cancelled(已取消)                                                                                                 | v1    |
| └─canceledAt                  | string | 订单取消时间                                                                                                                                                    | v1    |
| └─cancelReason                | string | 订单取消原因                                                                                                                                                    | v1    |
| └─orderNote                   | string | 订单备注                                                                                                                                                      | v1    |
| └─fulfillmentStatus           | string | 物流状态 initialled(空)，waiting(待发货)，partially\_shipped(部分发货)，shipped(已发货)，partially\_finished(部分完成)，finished(已完成), cancelled(取消)，returning(退货中)，returned(已退货) | v1    |
| └─customerDeletedAt           | string | 客户删除订单时间                                                                                                                                                  | v1    |
| └─placedAt                    | string | 订单确认时间                                                                                                                                                    | v1    |
| └─tags                        | string | 订单标签                                                                                                                                                      | v1    |
| └─discountCode                | string | 订单优惠码                                                                                                                                                     | v1    |
| └─codeDiscountTotal           | string | 订单优惠码优惠价格                                                                                                                                                 | v1    |
| └─lineItemDiscountTotal       | string | 商品折扣                                                                                                                                                      | v1    |
| └─customerNote                | string | 客户备注                                                                                                                                                      | v1    |
| └─totalDiscount               | string | 订单折扣                                                                                                                                                      | v1    |
| └─totalTax                    | string | 总税费                                                                                                                                                       | v1    |
| └─totalShipping               | string | 运费                                                                                                                                                        | v1    |
| └─createdAt                   | string | 创建时间                                                                                                                                                      | v1    |
| └─updatedAt                   | string | 更新时间                                                                                                                                                      | v1    |
| └─lineItems                   | array  | 订单商品                                                                                                                                                      | v1    |
|      └─productTitle           | string | 商品标题                                                                                                                                                      | v1    |
|      └─variantTitle           | string | 子商品标题                                                                                                                                                     | v1    |
|      └─quantity               | number | 商品数量                                                                                                                                                      | v1    |
|      └─note                   | string | 备注                                                                                                                                                        | v1    |
|      └─image                  | string | 商品图片                                                                                                                                                      | v1    |
|      └─price                  | string | 商品售价                                                                                                                                                      | v1    |
|      └─compareAtPrice         | string | 商品原价                                                                                                                                                      | v1    |
|      └─total                  | string | 总价                                                                                                                                                        | v1    |
|      └─sku                    | string | sku                                                                                                                                                       | v1    |
|      └─weight                 | string | 重量                                                                                                                                                        | v1    |
|      └─weightUnit             | string | 重量单位(kg, g ...)                                                                                                                                           | v1    |
|      └─vendor                 | string | 商品供应商                                                                                                                                                     | v1    |
|      └─properties             | string | 商品属性                                                                                                                                                      | v1    |
|      └─productUrl             | string | 商品url                                                                                                                                                     | v1    |
|      └─productHandle          | string | 商品handle                                                                                                                                                  | v1    |
|      └─id                     | number | id                                                                                                                                                        | v1    |
|      └─productId              | string | 商品id                                                                                                                                                      | v1    |
|      └─variantId              | string | 子商品id                                                                                                                                                     | v1    |
|      └─fulfillmentStatus      | string | 运单状态                                                                                                                                                      | v1    |
| └─paymentLine                 | object | 支付方式                                                                                                                                                      | v1    |
|      └─paymentChannel         | string | 支付渠道                                                                                                                                                      | v1    |
|      └─paymentMethod          | string | 支付方式                                                                                                                                                      | v1    |
|      └─transactionNo          | string | 交易号                                                                                                                                                       | v1    |
|      └─merchantId             | string | 收款账户ID                                                                                                                                                    | v1    |
|      └─merchantEmail          | string | 收款账户Email                                                                                                                                                 | v1    |
| └─shippingLine                | object | 运费方案                                                                                                                                                      | v1    |
|      └─name                   | string | 物流方案名称                                                                                                                                                    | v1    |
| └─billingAddress              | object | 账单地址                                                                                                                                                      | v1    |
|      └─firstName              | string | 收货人名                                                                                                                                                      | v1    |
|      └─lastName               | string | 收货人姓                                                                                                                                                      | v1    |
|      └─address1               | string | 街道                                                                                                                                                        | v1    |
|      └─address2               | string | 寓所                                                                                                                                                        | v1    |
|      └─city                   | string | 城市                                                                                                                                                        | v1    |
|      └─zip                    | string | 邮编                                                                                                                                                        | v1    |
|      └─province               | string | 省份                                                                                                                                                        | v1    |
|      └─country                | string | 国家                                                                                                                                                        | v1    |
|      └─company                | string | 公司                                                                                                                                                        | v1    |
|      └─latitude               | string | 纬度                                                                                                                                                        | v1    |
|      └─longitude              | string | 经度                                                                                                                                                        | v1    |
|      └─name                   | string | 姓名                                                                                                                                                        | v1    |
|      └─countryCode            | string | 国家代码                                                                                                                                                      | v1    |
|      └─provinceCode           | string | 省份代码                                                                                                                                                      | v1    |
|      └─phoneAreaCode          | string | 手机区号                                                                                                                                                      | v1    |
|      └─email                  | string | 邮箱                                                                                                                                                        | v1    |
|      └─area                   | string | 区域                                                                                                                                                        | v1    |
| └─shippingAddress             | object | 物流地址                                                                                                                                                      | v1    |
|      └─firstName              | string | 收货人名                                                                                                                                                      | v1    |
|      └─lastName               | string | 收货人姓                                                                                                                                                      | v1    |
|      └─address1               | string | 街道                                                                                                                                                        | v1    |
|      └─address2               | string | 寓所                                                                                                                                                        | v1    |
|      └─phone                  | string | 手机号码                                                                                                                                                      | v1    |
|      └─city                   | string | 城市                                                                                                                                                        | v1    |
|      └─zip                    | string | 邮编                                                                                                                                                        | v1    |
|      └─province               | string | 省份                                                                                                                                                        | v1    |
|      └─country                | string | 国家                                                                                                                                                        | v1    |
|      └─company                | string | 公司                                                                                                                                                        | v1    |
|      └─latitude               | string | 纬度                                                                                                                                                        | v1    |
|      └─longitude              | string | 经度                                                                                                                                                        | v1    |
|      └─name                   | string | 收货人姓名                                                                                                                                                     | v1    |
|      └─countryCode            | string | 国家代码                                                                                                                                                      | v1    |
|      └─provinceCode           | string | 省份代码                                                                                                                                                      | v1    |
|      └─phoneAreaCode          | string | 手机区号                                                                                                                                                      | v1    |
|      └─email                  | string | 邮箱                                                                                                                                                        | v1    |
|      └─area                   | string | 区域                                                                                                                                                        | v1    |
|      └─extraInfo              | string | 特殊物流字段                                                                                                                                                    | v1    |
| └─fulfillments                | array  | 运单信息                                                                                                                                                      | v1    |
|      └─id                     | number | id                                                                                                                                                        | v1    |
|      └─orderId                | number | 订单id                                                                                                                                                      | v1    |
|      └─status                 | string | 运单状态 waiting(待发货),shipped(已发货),finished(已完成),cancelled(已取消)                                                                                               | v1    |
|      └─createdAt              | string | 创建时间                                                                                                                                                      | v1    |
|      └─updatedAt              | string | 修改时间                                                                                                                                                      | v1    |
|      └─trackingCompany        | string | 物流公司                                                                                                                                                      | v1    |
|      └─trackingNumber         | string | 运单号                                                                                                                                                       | v1    |
|      └─trackingCompanyCode    | string | 物流公司编号                                                                                                                                                    | v1    |
|      └─lineItems              | array  | 测试                                                                                                                                                        | v1    |
|           └─productTitle      | string | 商品标题                                                                                                                                                      | v1    |
|           └─variantTitle      | string | 子商品标题                                                                                                                                                     | v1    |
|           └─quantity          | number | 商品数量                                                                                                                                                      | v1    |
|           └─note              | string | 备注                                                                                                                                                        | v1    |
|           └─image             | string | 商品图片                                                                                                                                                      | v1    |
|           └─price             | string | 商品售价                                                                                                                                                      | v1    |
|           └─compareAtPrice    | string | 商品原价                                                                                                                                                      | v1    |
|           └─total             | string | 总价                                                                                                                                                        | v1    |
|           └─sku               | string | sku                                                                                                                                                       | v1    |
|           └─weight            | string | 重量                                                                                                                                                        | v1    |
|           └─weightUnit        | string | 重量单位(kg, g ...)                                                                                                                                           | v1    |
|           └─vendor            | string | 商品供应商                                                                                                                                                     | v1    |
|           └─properties        | string | 商品属性                                                                                                                                                      | v1    |
|           └─productUrl        | string | 商品url                                                                                                                                                     | v1    |
|           └─productHandle     | string | 商品handle                                                                                                                                                  | v1    |
|           └─id                | number | id                                                                                                                                                        | v1    |
|           └─productId         | string | 商品id                                                                                                                                                      | v1    |
|           └─variantId         | string | 子商品id                                                                                                                                                     | v1    |
|           └─fulfillmentStatus | string | 运单状态                                                                                                                                                      | v1    |
| └─customer                    | object | 顾客信息                                                                                                                                                      | v1    |
|      └─email                  | string | 客户邮箱                                                                                                                                                      | v1    |
|      └─firstName              | string | 名                                                                                                                                                         | v1    |
|      └─lastName               | string | 姓                                                                                                                                                         | v1    |
|      └─ordersCount            | string | 客户下单数                                                                                                                                                     | v1    |
|      └─totalSpent             | string | 顾客消费总额                                                                                                                                                    | v1    |
|      └─phone                  | string | 客户手机号码                                                                                                                                                    | v1    |
|      └─createdAt              | string | 创建时间                                                                                                                                                      | v1    |
|      └─updatedAt              | string | 修改时间                                                                                                                                                      | v1    |

**Response-example:**

```json
{
    "code": 0,
    "errorCode": 0,
    "msg": "请求成功",
    "data": {
        "orderNo": "SVZ6191264",
        "id": "1376883403227529217",
        "totalPrice": "10.00",
        "subTotal": "11.00",
        "currency": "USD",
        "financialStatus": "waiting",
        "orderStatus": "opened",
        "canceledAt": null,
        "cancelReason": null,
        "orderNote": null,
        "fulfillmentStatus": "initialled",
        "customerDeletedAt": null,
        "placedAt": null,
        "tags": null,
        "discountCode": "KR88M4D7",
        "codeDiscountTotal": "1.00",
        "lineItemDiscountTotal": null,
        "customerNote": "",
        "totalDiscount": "1.00",
        "totalTax": "0.00",
        "totalShipping": "0.00",
        "createdAt": "2021-03-30 21:05:59",
        "updatedAt": "2021-03-31 09:15:39",
        "lineItems": [
            {
                "productTitle": "4444",
                "variantTitle": "4444",
                "quantity": 11,
                "note": null,
                "image": "https://cdn.shoptop.com/1357301923878989826.png",
                "price": "1.00",
                "compareAtPrice": "10.00",
                "total": "11.00",
                "sku": "111",
                "weight": "1.00",
                "weightUnit": "kg",
                "vendor": null,
                "properties": null,
                "productUrl": null,
                "productHandle": "4444",
                "id": "1376883403403689986",
                "productId": "1357302156562198530",
                "variantId": "1357302156591558657",
                "fulfillmentStatus": "waiting"
            }
        ],
        "paymentLine": {
            "paymentChannel": "ocean",
            "paymentMethod": "credit_card",
            "transactionNo": null,
            "merchantId": null,
            "merchantEmail": null
        },
        "shippingLine": {
            "name": "freeno"
        },
        "billingAddress": {
            "firstName": "",
            "lastName": "23 33",
            "address1": "323",
            "address2": "3242",
            "city": "3243242",
            "zip": "3333",
            "province": "Abyan",
            "country": "Yemen",
            "company": null,
            "latitude": null,
            "longitude": null,
            "name": "23 33",
            "countryCode": "YE",
            "provinceCode": "YE-AB",
            "phoneAreaCode": null,
            "email": "123@123.com",
            "area": null
        },
        "shippingAddress": {
            "firstName": "23 33",
            "lastName": "23 33",
            "address1": "323",
            "address2": "3242",
            "phone": "",
            "city": "3243242",
            "zip": "3333",
            "province": "Abyan",
            "country": "Yemen",
            "company": null,
            "latitude": null,
            "longitude": null,
            "name": "23 33 23 33",
            "countryCode": "YE",
            "provinceCode": "YE-AB",
            "phoneAreaCode": null,
            "email": "123@123.com",
            "area": null,
            "extraInfo": ""
        },
        "fulfillments": null,
        "customer": {
            "email": "1234@164.com",
            "firstName": "22423",
            "lastName": "23423",
            "ordersCount": "0",
            "totalSpent": "0.00",
            "phone": null,
            "createdAt": "2021-03-30 21:05:54",
            "updatedAt": null
        }
    }
}
```

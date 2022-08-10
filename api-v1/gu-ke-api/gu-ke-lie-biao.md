# 顾客列表

**URL:** /openapi/v1/customers/

**Type:** GET

**Content-Type:** application/x-www-form-urlencoded;charset=utf-8

**Description:** 顾客列表

**Query-parameters:**

| Parameter    | Type   | Description                      | Required | Since |
| ------------ | ------ | -------------------------------- | -------- | ----- |
| pageNo       | number | 页码，从1开始                          | true     | v1    |
| pageSize     | number | 每页显示条数 default: 10, maximum: 200 | true     | v1    |
| ids          | string | ids eg:100001,100002,100003      | false    | v1    |
| email        | string | 顾客邮箱                             | false    | v1    |
| createdAtMin | string | 创建起始时间 格式：yyyy-MM-dd HH:mm:ss    | false    | v1    |
| createdAtMax | string | 创建结束时间 格式：yyyy-MM-dd HH:mm:ss    | false    | v1    |
| updatedAtMin | string | 修改起始时间 格式：yyyy-MM-dd HH:mm:ss    | false    | v1    |
| updatedAtMax | string | 修改结束时间 格式：yyyy-MM-dd HH:mm:ss    | false    | v1    |

**Request-example:**

```
curl -X GET -k -i /openapi/v1/customers/?createdAtMin=2021-06-03 10:24:23&pageSize=10&createdAtMax=2021-08-03 10:24:23&email=vinnie@shoptop.com&ids=10,11&pageNo=1
```

**Response-fields:**

| Field               | Type    | Description                 | Since |
| ------------------- | ------- | --------------------------- | ----- |
| code                | number  | code                        | v1    |
| errorCode           | number  | errorCode                   | v1    |
| msg                 | string  | message                     | v1    |
| data                | array   | data                        | v1    |
| └─id                | number  | 顾客Id                        | v1    |
| └─firstName         | string  | 名                           | v1    |
| └─lastName          | string  | 姓                           | v1    |
| └─name              | string  | 姓名                          | v1    |
| └─email             | string  | 邮箱                          | v1    |
| └─phone             | string  | 手机号                         | v1    |
| └─acceptsMarketing  | boolean | 是否订阅接受营销                    | v1    |
| └─ordersCount       | number  | 订单数量                        | v1    |
| └─totalSpent        | string  | 消费总金额                       | v1    |
| └─tags              | string  | 标签                          | v1    |
| └─createdAt         | string  | 创建时间 格式：yyyy-MM-dd HH:mm:ss | v1    |
| └─updatedAt         | string  | 更新时间 格式：yyyy-MM-dd HH:mm:ss | v1    |
| └─defaultAddress    | object  | 默认地址                        | v1    |
|      └─id           | number  | 地址Id                        | v1    |
|      └─customerId   | number  | 顾客Id                        | v1    |
|      └─firstName    | string  | 名                           | v1    |
|      └─lastName     | string  | 姓                           | v1    |
|      └─name         | string  | 姓名                          | v1    |
|      └─email        | string  | 邮箱                          | v1    |
|      └─phone        | string  | 手机号                         | v1    |
|      └─company      | string  | 公司                          | v1    |
|      └─address1     | string  | 地址1                         | v1    |
|      └─address2     | string  | 地址2                         | v1    |
|      └─area         | string  | 区域                          | v1    |
|      └─city         | string  | 城市                          | v1    |
|      └─province     | string  | 省                           | v1    |
|      └─provinceCode | string  | 省代码                         | v1    |
|      └─country      | string  | 国家                          | v1    |
|      └─countryCode  | string  | 国家代码                        | v1    |
|      └─countryName  | string  | 国家名称                        | v1    |
|      └─zip          | string  | 邮编                          | v1    |
|      └─defaultFlag  | boolean | 是否默认地址                      | v1    |
| └─addresses         | array   | 地址列表                        | v1    |
|      └─id           | number  | 地址Id                        | v1    |
|      └─customerId   | number  | 名                           | v1    |
|      └─firstName    | string  | 名                           | v1    |
|      └─lastName     | string  | 姓                           | v1    |
|      └─name         | string  | 姓名                          | v1    |
|      └─email        | string  | 邮箱                          | v1    |
|      └─phone        | string  | 手机号                         | v1    |
|      └─company      | string  | 公司                          | v1    |
|      └─address1     | string  | 地址1                         | v1    |
|      └─address2     | string  | 地址2                         | v1    |
|      └─area         | string  | 区域                          | v1    |
|      └─city         | string  | 城市                          | v1    |
|      └─province     | string  | 省                           | v1    |
|      └─provinceCode | string  | 省代码                         | v1    |
|      └─country      | string  | 国家                          | v1    |
|      └─countryCode  | string  | 国家代码                        | v1    |
|      └─countryName  | string  | 国家名称                        | v1    |
|      └─zip          | string  | 邮编                          | v1    |
|      └─defaultFlag  | boolean | 是否默认地址                      | v1    |

**Response-example:**

```
{
    "code": 0,
    "errorCode": 0,
    "msg": "请求成功",
    "data": [
        {
            "id": 55,
            "firstName": "Vinnie",
            "lastName": "Li",
            "name": "Vinnie Li",
            "email": "vinnie@shoptop.com",
            "phone": "15808728191",
            "acceptsMarketing": true,
            "ordersCount": 282,
            "totalSpent": "655.69",
            "tags": "3w1lh0",
            "createdAt": "tlp4vk",
            "updatedAt": "09w7w1",
            "defaultAddress": {
                "id": 896,
                "customerId": 468,
                "firstName": "Vinnie",
                "lastName": "Li",
                "name": "Vinnie Li",
                "email": "vinnie@shoptop.com",
                "phone": "15808728191",
                "company": "shoptop",
                "address1": "3sphg9",
                "address2": "vao0fc",
                "area": "sck117",
                "city": "1fqsup",
                "province": "uwh1ix",
                "provinceCode": "19456",
                "country": "china",
                "countryCode": "CN",
                "countryName": "china",
                "zip": "230001",
                "defaultFlag": true
            },
            "addresses": [
                {
                    "id": 523,
                    "customerId": 1,
                    "firstName": "Vinnie",
                    "lastName": "Li",
                    "name": "Vinnie Li",
                    "email": "vinnie@shoptop.com",
                    "phone": "15808728191",
                    "company": "shoptop",
                    "address1": "3sphg9",
                    "address2": "vao0fc",
                    "area": "sck117",
                    "city": "1fqsup",
                    "province": "uwh1ix",
                    "provinceCode": "19456",
                    "country": "china",
                    "countryCode": "CN",
                    "countryName": "china",
                    "zip": "230001",
                    "defaultFlag": false
                }
            ]
        }
    ]
}
```

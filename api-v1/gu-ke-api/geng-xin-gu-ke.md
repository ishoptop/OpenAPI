# 更新顾客

**URL:** /openapi/v1/customers/{id}

**Type:** PUT

**Content-Type:** application/json; charset=utf-8

**Description:** 更新顾客

**Path-parameters:**

| Parameter | Type   | Description        | Required | Since |
| --------- | ------ | ------------------ | -------- | ----- |
| id        | number | No comments found. | true     | -     |

**Body-parameters:**

| Parameter            | Type    | Description | Required | Since |
| -------------------- | ------- | ----------- | -------- | ----- |
| email                | string  | 邮箱          | true     | v1    |
| firstName            | string  | 名           | false    | v1    |
| lastName             | string  | 姓           | false    | v1    |
| phone                | string  | 手机          | false    | v1    |
| phoneAreaCode        | string  | 手机区号        | false    | v1    |
| acceptsMarketing     | boolean | 是否订阅接受营销    | false    | v1    |
| password             | string  | 密码          | false    | v1    |
| passwordConfirmation | string  | 确认密码        | false    | v1    |
| tags                 | string  | 标签          | false    | v1    |
| address              | object  | 顾客地址        | false    | v1    |
| └─firstName          | string  | 名           | false    | v1    |
| └─lastName           | string  | 姓           | false    | v1    |
| └─email              | string  | 邮箱          | true     | v1    |
| └─address1           | string  | 地址1         | false    | v1    |
| └─address2           | string  | 地址2         | false    | v1    |
| └─area               | string  | 区域          | false    | v1    |
| └─city               | string  | 城市          | false    | v1    |
| └─province           | string  | 省           | false    | v1    |
| └─provinceCode       | string  | 省代码         | false    | v1    |
| └─country            | string  | 国家          | false    | v1    |
| └─countryCode        | string  | 国家代码        | false    | v1    |
| └─company            | string  | 公司          | false    | v1    |
| └─phone              | string  | 手机          | false    | v1    |
| └─phoneAreaCode      | string  | 手机区号        | false    | v1    |
| └─zip                | string  | 邮编          | false    | v1    |
| └─defaultFlag        | boolean | 是否默认地址      | true     | v1    |

**Request-example:**

```
curl -X PUT -k -H 'Content-Type: application/json; charset=utf-8' -i /openapi/v1/customers/951 --data '{
    "email": "vinnie@shoptop.com",
    "firstName": "Vinnie",
    "lastName": "Li",
    "phone": "15808728191",
    "phoneAreaCode": "+86",
    "acceptsMarketing": true,
    "password": "cgqny6",
    "passwordConfirmation": "okg9v7",
    "tags": "y3ut9g",
    "address": {
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
    }
}'
```

**Response-fields:**

| Field               | Type    | Description                 | Since |
| ------------------- | ------- | --------------------------- | ----- |
| code                | number  | code                        | v1    |
| errorCode           | number  | errorCode                   | v1    |
| msg                 | string  | message                     | v1    |
| data                | object  | data                        | v1    |
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
    "data": {
        "id": 659,
        "firstName": "Vinnie",
        "lastName": "Li",
        "name": "Vinnie Li",
        "email": "vinnie@shoptop.com",
        "phone": "15808728191",
        "acceptsMarketing": true,
        "ordersCount": 29,
        "totalSpent": "126",
        "tags": "iogox5",
        "createdAt": "ww0lmo",
        "updatedAt": "ql3i87",
        "defaultAddress": {
            "id": 502,
            "customerId": 891,
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
                "id": 867,
                "customerId": 403,
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
}
```

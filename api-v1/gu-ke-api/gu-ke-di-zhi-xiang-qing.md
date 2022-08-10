# 顾客地址详情

**URL:** /openapi/v1/customers/{customerId}/addresses/{addressId}

**Type:** GET

**Content-Type:** application/x-www-form-urlencoded;charset=utf-8

**Description:** 顾客地址详情

**Path-parameters:**

| Parameter  | Type   | Description        | Required | Since |
| ---------- | ------ | ------------------ | -------- | ----- |
| customerId | number | No comments found. | true     | -     |
| addressId  | number | No comments found. | true     | -     |

**Request-example:**

```
curl -X GET -k -i /openapi/v1/customers/510/addresses/137
```

**Response-fields:**

| Field          | Type    | Description | Since |
| -------------- | ------- | ----------- | ----- |
| code           | number  | code        | v1    |
| errorCode      | number  | errorCode   | v1    |
| msg            | string  | message     | v1    |
| data           | object  | data        | v1    |
| └─id           | number  | 地址Id        | v1    |
| └─customerId   | number  | 名           | v1    |
| └─firstName    | string  | 名           | v1    |
| └─lastName     | string  | 姓           | v1    |
| └─name         | string  | 姓名          | v1    |
| └─email        | string  | 邮箱          | v1    |
| └─phone        | string  | 手机号         | v1    |
| └─company      | string  | 公司          | v1    |
| └─address1     | string  | 地址1         | v1    |
| └─address2     | string  | 地址2         | v1    |
| └─area         | string  | 区域          | v1    |
| └─city         | string  | 城市          | v1    |
| └─province     | string  | 省           | v1    |
| └─provinceCode | string  | 省代码         | v1    |
| └─country      | string  | 国家          | v1    |
| └─countryCode  | string  | 国家代码        | v1    |
| └─countryName  | string  | 国家名称        | v1    |
| └─zip          | string  | 邮编          | v1    |
| └─defaultFlag  | boolean | 是否默认地址      | v1    |

**Response-example:**

```
{
    "code": 102,
    "errorCode": 91,
    "msg": "r1uf9m",
    "data": {
        "id": 933,
        "customerId": 351,
        "firstName": "Vinnie",
        "lastName": "Li",
        "name": "Vinnie Li",
        "email": "vinnie@shoptop.com",
        "phone": "15808728191",
        "company": "shoptop",
        "address1": "k2o9jo",
        "address2": "ts98di",
        "area": "uhwi7i",
        "city": "hfcpht",
        "province": "u2filv",
        "provinceCode": "19456",
        "country": "china",
        "countryCode": "CN",
        "countryName": "china",
        "zip": "230001",
        "defaultFlag": true
    }
}
```

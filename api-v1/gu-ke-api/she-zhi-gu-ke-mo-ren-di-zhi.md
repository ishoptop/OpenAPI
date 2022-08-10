# 设置顾客默认地址

**URL:** /openapi/v1/customers/{customerId}/addresses/{addressId}/default

**Type:** PUT

**Content-Type:** application/x-www-form-urlencoded;charset=utf-8

**Description:** 设置顾客默认地址

**Path-parameters:**

| Parameter  | Type   | Description        | Required | Since |
| ---------- | ------ | ------------------ | -------- | ----- |
| customerId | number | No comments found. | true     | -     |
| addressId  | number | No comments found. | true     | -     |

**Request-example:**

```
curl -X PUT -k -i /openapi/v1/customers/833/addresses/156/default
```

**Response-fields:**

| Field     | Type   | Description | Since |
| --------- | ------ | ----------- | ----- |
| code      | number | code        | v1    |
| errorCode | number | errorCode   | v1    |
| msg       | string | message     | v1    |
| data      | object | data        | v1    |

**Response-example:**

```
{
    "code": 0,
    "errorCode": 0,
    "msg": "请求成功",
    "data": true
}
```

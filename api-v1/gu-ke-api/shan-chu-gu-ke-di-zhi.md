# 删除顾客地址

**URL:** /openapi/v1/customers/{customerId}/addresses/{addressId}

**Type:** DELETE

**Content-Type:** application/x-www-form-urlencoded;charset=utf-8

**Description:** 删除顾客地址

**Path-parameters:**

| Parameter  | Type   | Description | Required | Since |
| ---------- | ------ | ----------- | -------- | ----- |
| customerId | number | 顾客Id.       | true     | -     |
| addressId  | number | 地址Id.       | true     | -     |

**Request-example:**

```
curl -X DELETE -k -i /openapi/v1/customers/249/addresses/755
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

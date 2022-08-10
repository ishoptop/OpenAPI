# 店铺脚本数量

**URL:** /openapi/v1/script/tags/count

**Type:** GET

**Content-Type:** application/x-www-form-urlencoded;charset=utf-8

**Description:** 脚本数量

**Request-headers:**

| Header       | Type   | Description        | Required | Since |
| ------------ | ------ | ------------------ | -------- | ----- |
| Access-Token | string | No comments found. | true     | -     |

**Request-example:**

```
curl -X GET -k -H 'Access-Token' -i /openapi/v1/script/tags/count
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

```
{
    "code": 0,
    "errorCode": 0,
    "msg": "请求成功",
    "data": {
        "count": 1
    }
}
```

# 删除店铺脚本

**URL:** /openapi/v1/script/tags/{id}

**Type:** DELETE

**Content-Type:** application/x-www-form-urlencoded;charset=utf-8

**Description:** 删除脚本

**Path-parameters:**

| Parameter | Type   | Description        | Required | Since |
| --------- | ------ | ------------------ | -------- | ----- |
| id        | number | No comments found. | true     | -     |

**Request-example:**

```
curl -X DELETE -k -i /openapi/v1/script/tags/233
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

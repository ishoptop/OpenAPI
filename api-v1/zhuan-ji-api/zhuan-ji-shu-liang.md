# 专辑数量

**URL:** /openapi/v1/collections/count

**Type:** GET

**Content-Type:** application/x-www-form-urlencoded;charset=utf-8

**Description:** 专辑数量

**Query-parameters:**

| Parameter | Type   | Description | Required | Since |
| --------- | ------ | ----------- | -------- | ----- |
| keyword   | string | 搜索关键词       | false    | v1    |
| shopId    | number | 店铺id        | false    | v1    |

**Request-example:**

```
curl -X GET -i /openapi/v1/collections/count?shopId=321&keyword=shfn0c
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

```json
{
    "code": 0,
    "errorCode": 0,
    "msg": "请求成功",
    "data": {
        "count": "27"
    }
}
```

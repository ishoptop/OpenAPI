# 商品数量

**URL:** /openapi/v1/products/count

**Type:** GET

**Content-Type:** application/x-www-form-urlencoded;charset=utf-8

**Description:** 商品数量

**Query-parameters:**

| Parameter       | Type   | Description              | Required | Since |
| --------------- | ------ | ------------------------ | -------- | ----- |
| published       | number | 商品是否已发布,0:未发布,1:已发布,2:全部 | false    | v1    |
| keyword         | string | 搜索关键词                    | false    | v1    |
| shopId          | number | 店铺id                     | false    | v1    |
| beginCreateTime | string | 创建时间开始时间                 | false    | v1    |
| endCreateTime   | string | 创建时间结束时间                 | false    | v1    |

**Request-example:**

```
curl -X GET -i /openapi/v1/products/count?keyword=xb6f9y&shopId=205&endCreateTime=2021-08-12 09:29:38&published=220&beginCreateTime=2021-08-12 09:29:38
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
        "count": "88"
    }
}
```

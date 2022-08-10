# 店铺脚本详情

**URL:** /openapi/v1/script/tags/{id}

**Type:** GET

**Content-Type:** application/x-www-form-urlencoded;charset=utf-8

**Description:** 脚本详情

**Path-parameters:**

| Parameter | Type   | Description        | Required | Since |
| --------- | ------ | ------------------ | -------- | ----- |
| id        | number | No comments found. | true     | -     |

**Request-example:**

```
curl -X GET -k -i /openapi/v1/script/tags/122
```

**Response-fields:**

| Field          | Type   | Description                                                          | Since |
| -------------- | ------ | -------------------------------------------------------------------- | ----- |
| code           | number | code                                                                 | v1    |
| errorCode      | number | errorCode                                                            | v1    |
| msg            | string | message                                                              | v1    |
| data           | object | data                                                                 | v1    |
| └─id           | number | id                                                                   | v1    |
| └─script       | string | 脚本                                                                   | v1    |
| └─displayScope | string | 展示范围 eg:all,index,collection,product,cart,coupon,search,checkout,404 | v1    |
| └─eventType    | string | 事件类型 eg:app                                                          | v1    |

**Response-example:**

```
{
    "code": 0,
    "errorCode": 0,
    "msg": "请求成功",
    "data": {
        "id": 327,
        "script": "<script src=\"https://ishoptop.com/test2.js\"></script>",
        "displayScope": "all",
        "eventType": "app"
    }
}
```

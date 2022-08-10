# 店铺脚本列表

**URL:** /openapi/v1/script/tags/

**Type:** GET

**Content-Type:** application/x-www-form-urlencoded;charset=utf-8

**Description:** 脚本列表

**Request-headers:**

| Header       | Type   | Description | Required | Since |
| ------------ | ------ | ----------- | -------- | ----- |
| Access-Token | string | null        | true     | -     |

**Query-parameters:**

| Parameter | Type   | Description                      | Required | Since |
| --------- | ------ | -------------------------------- | -------- | ----- |
| pageNo    | number | 页码，从1开始                          | true     | v1    |
| pageSize  | number | 每页显示条数 default: 10, maximum: 200 | true     | v1    |
| eventType | string | 事件类型 eg:app                      | false    | v1    |

**Request-example:**

```
curl -X GET -k -H 'Access-Token' -i /openapi/v1/script/tags/?pageSize=10&pageNo=1&eventType=app
```

**Response-fields:**

| Field          | Type   | Description                                                          | Since |
| -------------- | ------ | -------------------------------------------------------------------- | ----- |
| code           | number | code                                                                 | v1    |
| errorCode      | number | errorCode                                                            | v1    |
| msg            | string | message                                                              | v1    |
| data           | array  | data                                                                 | v1    |
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
    "data": [
        {
            "id": 666,
            "script": "<script src=\"https://ishoptop.com/test2.js\"></script>",
            "displayScope": "all",
            "eventType": "app"
        }
    ]
}
```

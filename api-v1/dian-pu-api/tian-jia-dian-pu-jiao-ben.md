# 添加店铺脚本

**URL:** /openapi/v1/script/tags/

**Type:** POST

**Content-Type:** application/json; charset=utf-8

**Description:** 添加脚本

**Request-headers:**

| Header       | Type   | Description | Required | Since |
| ------------ | ------ | ----------- | -------- | ----- |
| Access-Token | string | null        | true     | -     |

**Body-parameters:**

| Parameter    | Type   | Description                                                          | Required | Since |
| ------------ | ------ | -------------------------------------------------------------------- | -------- | ----- |
| script       | string | 脚本                                                                   | true     | v1    |
| displayScope | string | 展示范围 eg:all,index,collection,product,cart,coupon,search,checkout,404 | true     | v1    |
| eventType    | string | 事件类型 eg:app                                                          | true     | v1    |

**Request-example:**

```
curl -X POST -k -H 'Content-Type: application/json; charset=utf-8' -H 'Access-Token' -i /openapi/v1/script/tags/ --data '{
    "script": "<script src=\"https://ishoptop.com/test.js\"></script>",
    "displayScope": "all",
    "eventType": "app"
}'
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
        "id": "10001",
        "script": "<script src=\"https://ishoptop.com/test.js\"></script>",
        "displayScope": "all",
        "eventType": "app"
    }
}
```

# 创建商品

**URL:** /openapi/v1/products/

**Type:** POST

**Content-Type:** application/json; charset=utf-8

**Description:** 创建商品

**Body-parameters:**

| Parameter           | Type   | Description                                 | Required | Since |
| ------------------- | ------ | ------------------------------------------- | -------- | ----- |
| spuId               | number | 商品spuID                                     | false    | v1    |
| seoTitle            | string | seo标题                                       | false    | v1    |
| seoKeywords         | string | seo关键词                                      | false    | v1    |
| seoDescription      | string | seo描述                                       | false    | v1    |
| handle              | string | 商品url尾缀                                     | false    | v1    |
| goodsTitle          | string | 商品标题                                        | false    | v1    |
| goodsBrief          | string | 副标题                                         | false    | v1    |
| spu                 | string | spu属性                                       | false    | v1    |
| inventoryTracking   | number | 是否跟踪库存,0:不跟踪,1:跟踪                           | false    | v1    |
| inventoryPolicy     | number | 跟踪库存策略,1:库存为0时不允许购买,2:库存为0时允许购买,3:库存为0时自动下架 | false    | v1    |
| needVariantImage    | number | sku款式是否需要配图,1:需要,0:不需要                      | false    | v1    |
| published           | number | 是否上架                                        | false    | v1    |
| publishedAt         | string | 上架时间                                        | false    | v1    |
| requiresShipping    | number | 是否需要物流                                      | false    | v1    |
| taxable             | number | 是否对此商品收税                                    | false    | v1    |
| vendorName          | string | 供应商名称                                       | false    | v1    |
| vendorUrl           | string | 供应商url                                      | false    | v1    |
| amazonLink          | string | 亚马逊商品链接                                     | false    | v1    |
| shopId              | number | 店铺id                                        | false    | v1    |
| goodsDescription    | string | 商品描述                                        | false    | v1    |
| isFreeShipping      | number | 是否免运费(0不免运费,1免运费)                           | false    | v1    |
| isSensitiveGoods    | number | 是否为敏感商品                                     | false    | v1    |
| skus                | array  | 商品sku列表                                     | false    | v1    |
| └─skuId             | number | 商品skuID                                     | false    | v1    |
| └─spuId             | number | 店铺id                                        | false    | v1    |
| └─barcode           | string | 条形码                                         | false    | v1    |
| └─shopId            | number | 店铺id                                        | false    | v1    |
| └─compareAtPrice    | number | 原价                                          | false    | v1    |
| └─price             | number | 售价                                          | false    | v1    |
| └─inventoryQuantity | number | 库存                                          | false    | v1    |
| └─skuNote           | string | 备注                                          | false    | v1    |
| └─sku               | string | sku属性                                       | false    | v1    |
| └─skuImage          | string | 图片                                          | false    | v1    |
| └─specOption1       | string | 规格属性1                                       | false    | v1    |
| └─specOption2       | string | 规格属性2                                       | false    | v1    |
| └─specOption3       | string | 规格属性3                                       | false    | v1    |
| └─weight            | number | 重量                                          | false    | v1    |
| └─weightUnit        | string | 重量单位                                        | false    | v1    |
| imageUrls           | array  | 商品图片列表(第一张是主图）                              | false    | v1    |
| specs               | array  | 商品规格列表                                      | false    | v1    |
| └─spuSpecName       | string | 规格名称                                        | false    | v1    |
| └─position          | number | 规格顺序                                        | false    | v1    |
| └─spuSpecValues     | array  | 规格值                                         | false    | v1    |
| goodsTags           | array  | 商品标签                                        | false    | v1    |
| isSingleSku         | number | 是否单一款式                                      | false    | v1    |
| inventoryQuantity   | number | 库存数量                                        | false    | v1    |

**Request-example:**

```
curl -X POST -H 'Content-Type: application/json; charset=utf-8' -i /openapi/v1/products/ --data '{
    "spuId": 2b3d272d-12b5-4133-bbb0-5e43e748c730,
    "seoTitle": "7u405b",
    "seoKeywords": "72vhiz",
    "seoDescription": "vbf73k",
    "handle": "mt1aiu",
    "goodsTitle": "win3i8",
    "goodsBrief": "25dzw6",
    "spu": "phphza",
    "inventoryTracking": 321,
    "inventoryPolicy": 521,
    "needVariantImage": 29,
    "published": 839,
    "publishedAt": "2021-08-12 09:29:39",
    "requiresShipping": 196,
    "taxable": 509,
    "vendorName": "玛丽",
    "vendorUrl": "www.shoptop.com",
    "amazonLink": "ue4bb5",
    "shopId": 610,
    "goodsDescription": "z5u1j1",
    "isFreeShipping": 21,
    "isSensitiveGoods": 48,
    "skus": [
        {
            "skuId": 2b3d272d-12b5-4133-bbb0-5e43e748c730,
            "spuId": 2b3d272d-12b5-4133-bbb0-5e43e748c730,
            "barcode": "79665",
            "shopId": 531,
            "compareAtPrice": 187,
            "price": 169,
            "inventoryQuantity": 450,
            "skuNote": "lspe8w",
            "sku": "9cn7vk",
            "skuImage": "dw72cc",
            "specOption1": "64exvb",
            "specOption2": "3i0mo3",
            "specOption3": "41uw9d",
            "weight": 623,
            "weightUnit": "qinlyv"
        }
    ],
    "imageUrls": [
        "6y32nw"
    ],
    "specs": [
        {
            "spuSpecName": "健柏罗",
            "position": 172,
            "spuSpecValues": [
                "y0xt71"
            ]
        }
    ],
    "goodsTags": [
        "0y4boa"
    ],
    "isSingleSku": 159,
    "inventoryQuantity": 472
}'
```

**Response-fields:**

| Field     | Type   | Description | Since |
| --------- | ------ | ----------- | ----- |
| code      | number | code        | v1    |
| errorCode | number | errorCode   | v1    |
| msg       | string | message     | v1    |
| data      | object | data        | v1    |
| └─status  | string | 状态          | v1    |

**Response-example:**

```json
{
    "code": 0,
    "errorCode": 0,
    "msg": "请求成功",
    "data": {
        "status": "success"
    }
}
```

# 商品列表

**URL:** /openapi/v1/products/

**Type:** GET

**Content-Type:** application/x-www-form-urlencoded;charset=utf-8

**Description:** 商品列表

**Query-parameters:**

| Parameter       | Type   | Description                      | Required | Since |
| --------------- | ------ | -------------------------------- | -------- | ----- |
| pageNo          | number | 页码，从1开始                          | true     | v1    |
| pageSize        | number | 每页显示条数 default: 10, maximum: 200 | true     | v1    |
| published       | number | 商品是否已发布,0:未发布,1:已发布,2:全部         | false    | v1    |
| keyword         | string | 搜索关键词                            | false    | v1    |
| shopId          | number | 店铺id                             | false    | v1    |
| beginCreateTime | string | 创建时间开始时间                         | false    | v1    |
| endCreateTime   | string | 创建时间结束时间                         | false    | v1    |

**Request-example:**

```
curl -X GET -i /openapi/v1/products/?endCreateTime=2021-08-12 09:29:38&published=144&shopId=497&pageSize=10&pageNo=856&keyword=ezt65m&beginCreateTime=2021-08-12 09:29:38
```

**Response-fields:**

| Field                        | Type   | Description                                 | Since |
| ---------------------------- | ------ | ------------------------------------------- | ----- |
| code                         | number | code                                        | v1    |
| errorCode                    | number | errorCode                                   | v1    |
| msg                          | string | message                                     | v1    |
| data                         | array  | data                                        | v1    |
| └─spuId                      | number | 商品spuID                                     | v1    |
| └─seoTitle                   | string | seo标题                                       | v1    |
| └─seoKeywords                | string | seo关键词                                      | v1    |
| └─seoDescription             | string | seo描述                                       | v1    |
| └─handle                     | string | 商品url尾缀                                     | v1    |
| └─goodsImage                 | object | 商品主图                                        | v1    |
|      └─fileRepositoryId      | number | 图片文件id                                      | v1    |
|      └─path                  | string | 图片位置                                        | v1    |
|      └─url                   | string | 图片url                                       | v1    |
|      └─height                | number | 高度                                          | v1    |
|      └─width                 | number | 宽度                                          | v1    |
|      └─type                  | string | 文件格式类型                                      | v1    |
| └─goodsTitle                 | string | 商品标题                                        | v1    |
| └─goodsBrief                 | string | 副标题                                         | v1    |
| └─spu                        | string | spu属性                                       | v1    |
| └─inventoryTracking          | number | 是否跟踪库存,1:跟踪,0:不跟踪                           | v1    |
| └─inventoryPolicy            | number | 跟踪库存策略,1:库存为0时不允许购买,2:库存为0时允许购买,3:库存为0时自动下架 | v1    |
| └─needVariantImage           | number | sku款式是否需要配图,0:不需要,1:需要                      | v1    |
| └─published                  | number | 是否上架,1:已上架,0:已下架                            | v1    |
| └─publishedAt                | string | 上架时间                                        | v1    |
| └─requiresShipping           | number | 是否需要物流                                      | v1    |
| └─taxable                    | number | 是否对此商品收税                                    | v1    |
| └─vendorName                 | string | 供应商名称                                       | v1    |
| └─vendorUrl                  | string | 供应商url                                      | v1    |
| └─amazonLink                 | string | 亚马逊商品链接                                     | v1    |
| └─shopId                     | number | 店铺id                                        | v1    |
| └─goodsDescription           | string | 商品描述                                        | v1    |
| └─isFreeShipping             | number | 是否免运费(0不免运费,1免运费)                           | v1    |
| └─isSensitiveGoods           | number | 是否为敏感商品                                     | v1    |
| └─isSingleSku                | number | 是否单一款式                                      | v1    |
| └─inventoryQuantity          | number | 库存数量                                        | v1    |
| └─createTime                 | string | 创建时间                                        | v1    |
| └─updateTime                 | string | 修改时间                                        | v1    |
| └─collections                | array  | 商品所属的专辑                                     | v1    |
|      └─collectionId          | number | 商品专辑id                                      | v1    |
|      └─collectionTitle       | string | 商品专辑标题                                      | v1    |
|      └─smart                 | number | 是否使用智能添加                                    | v1    |
| └─skus                       | array  | 子商品                                         | v1    |
|      └─skuId                 | number | 子商品id                                       | v1    |
|      └─spuId                 | number | 店铺id                                        | v1    |
|      └─barcode               | string | 条形码                                         | v1    |
|      └─shopId                | number | 店铺id                                        | v1    |
|      └─compareAtPrice        | number | 原价                                          | v1    |
|      └─price                 | number | 售价                                          | v1    |
|      └─inventoryQuantity     | number | 库存                                          | v1    |
|      └─skuNote               | string | 备注                                          | v1    |
|      └─sku                   | string | sku属性                                       | v1    |
|      └─skuImage              | object | 图片数据                                        | v1    |
|           └─fileRepositoryId | number | 图片文件id                                      | v1    |
|           └─path             | string | 图片位置                                        | v1    |
|           └─url              | string | 图片url                                       | v1    |
|           └─height           | number | 高度                                          | v1    |
|           └─width            | number | 宽度                                          | v1    |
|           └─type             | string | 文件格式类型                                      | v1    |
|      └─specOption1           | string | 规格属性1                                       | v1    |
|      └─specOption2           | string | 规格属性2                                       | v1    |
|      └─specOption3           | string | 规格属性3                                       | v1    |
|      └─weight                | number | 重量                                          | v1    |
|      └─weightUnit            | string | 重量单位                                        | v1    |
| └─images                     | array  | 商品图片列表                                      | v1    |
|      └─position              | number | 图片排序/位置                                     | v1    |
|      └─imageData             | object | 图片数据                                        | v1    |
|           └─fileRepositoryId | number | 图片文件id                                      | v1    |
|           └─path             | string | 图片位置                                        | v1    |
|           └─url              | string | 图片url                                       | v1    |
|           └─height           | number | 高度                                          | v1    |
|           └─width            | number | 宽度                                          | v1    |
|           └─type             | string | 文件格式类型                                      | v1    |
| └─specs                      | array  | 商品属性                                        | v1    |
|      └─spuSpecName           | string | 规格名称                                        | v1    |
|      └─position              | string | 规格位置,1,2,3                                  | v1    |
|      └─spuSpecValues         | array  | 商品规格属性                                      | v1    |
| └─goodsTags                  | array  | 商品标签                                        | v1    |

**Response-example:**

```json
{
    "code": 0,
    "errorCode": 0,
    "msg": "请求成功",
    "data": [
        {
            "spuId": "1425655086029709313",
            "seoTitle": "High-performance backpacks for backpacks, hiking, and camping",
            "seoKeywords": "",
            "seoDescription": "High-performance backpacks for backpacks, hiking, and camping",
            "handle": "High-performance-backpacks-for-backpacks-hiking-and-camping_1s25",
            "goodsImage": {
                "fileRepositoryId": "1357301923878989826",
                "path": "1357301923878989826.png",
                "url": "https://cdn.shoptop.com/1357301923878989826.png",
                "height": 239,
                "width": 378,
                "type": "image/png"
            },
            "goodsTitle": "High-performance backpacks for backpacks, hiking, and camping",
            "goodsBrief": "High-performance backpacks for backpacks, hiking, and camping",
            "spu": "",
            "inventoryTracking": 0,
            "inventoryPolicy": 2,
            "needVariantImage": 0,
            "published": 1,
            "publishedAt": null,
            "requiresShipping": 1,
            "taxable": 0,
            "vendorName": null,
            "vendorUrl": null,
            "amazonLink": null,
            "shopId": 100103,
            "goodsDescription": "<p class=\"p1\" .... bags for strategic packaging</p>",
            "isFreeShipping": 0,
            "isSensitiveGoods": 0,
            "isSingleSku": 1,
            "inventoryQuantity": 0,
            "createTime": "2021-08-12 11:07:15",
            "updateTime": "2021-08-12 11:07:15",
            "collections": null,
            "skus": [
                {
                    "skuId": "1425655086088429570",
                    "spuId": "1425655086029709313",
                    "barcode": "111",
                    "shopId": 100103,
                    "compareAtPrice": 10000,
                    "price": 10000,
                    "inventoryQuantity": 0,
                    "skuNote": null,
                    "sku": "11",
                    "skuImage": null,
                    "specOption1": null,
                    "specOption2": null,
                    "specOption3": null,
                    "weight": 1.00,
                    "weightUnit": "kg"
                }
            ],
            "images": [
                {
                    "position": 0,
                    "imageData": {
                        "fileRepositoryId": "1357301923878989826",
                        "path": "1357301923878989826.png",
                        "url": "https://cdn.shoptop.com/1357301923878989826.png",
                        "height": 239,
                        "width": 378,
                        "type": "image/png"
                    }
                }
            ],
            "specs": [],
            "goodsTags": []
        }
    ]
}
```

# Webhooks验签

{% hint style="info" %}
每个webhook请求都会带有一个通过base64加密的**X-Shoptop-Hmac-Sha256**请求头。**X-Shoptop-Hmac-Sha256**的值是使用插件的Client Secret和请求中带有的参数生成的。如果需要验证请求是来自Shoptop，可以按照SDK中的算法计算出HMAC值，并和请求头中的**X-Shoptop-Hmac-Sha256**值进行比较，如果相同，则可以确认请求来自Shoptop。通过Hmac算法，使用请求中的数据和Client Secret计算出hmac值，再经过Base64处理，即可得到HMAC值。
{% endhint %}

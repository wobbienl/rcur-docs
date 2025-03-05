# Get product

<mark style="color:blue;">`GET`</mark> `https://rcur.app/api/v2/products/{id}`

#### Path Parameters

| Name                                   | Type   | Description           |
| -------------------------------------- | ------ | --------------------- |
| {id}<mark style="color:red;">\*</mark> | String | The ID of the product |

{% tabs %}
{% tab title="200: OK " %}
<pre class="language-json"><code class="lang-json">{
    "id": "ybWEyDp4oe",
    "name": "Test abbo",
    "type": "subscription",
    "amount": "5.00",
    "currency": "EUR",
    "interval": "1 months",
    "times": <a data-footnote-ref href="#user-content-fn-1">4</a>,
    "wc_product_id": 1434
}
</code></pre>
{% endtab %}

{% tab title="404: Not Found " %}
```json
{
    "status": 404,
    "error": "Product not found"
}
```
{% endtab %}
{% endtabs %}

[^1]: If `0`, the subscription will not stop automatically

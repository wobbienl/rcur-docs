# Create product

<mark style="color:green;">`POST`</mark> `https://rcur.app/api/v2/products`

#### Request Body

| Name                                     | Type              | Description                                                                                                                                                                  |
| ---------------------------------------- | ----------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| name<mark style="color:red;">\*</mark>   | String            | The name of the product                                                                                                                                                      |
| type<mark style="color:red;">\*</mark>   | Enum              | Possible values: `once` `subscription` `shipping_costs`                                                                                                                      |
| amount<mark style="color:red;">\*</mark> | Double            | The amount of the product. Example: `14.99`                                                                                                                                  |
| vat<mark style="color:red;">\*</mark>    | Integer \| String | The VAT in percentage. If using an invoice integration, use the ID of the Get VAT response.                                                                                  |
| interval                                 | Enum              | Required if `type` is `subscription` Possible values: `months` `weeks` `days` `years`                                                                                        |
| interval\_value                          | Integer           | Required if `type` is `subscription` The quantity of the interval. For example, when `interval` is set to `months` and `interval_value` to `1` it will be a monthly product. |
| times                                    | Integer           | Only applicable when `type` is `subscription` . When not provided, the product subscription will be continuously.                                                            |
| woocommerce\_product\_id                 | Integer           | Only applicable when WooCommerce integration enabled. The product ID or variation ID of the WooCommerce product.                                                             |

{% tabs %}
{% tab title="422: Unprocessable Entity " %}
<pre class="language-json"><code class="lang-json"><strong>{
</strong>    "status": 422,
    "error": "Could not create product. Some fields contain invalid data",
    "fields": {
        "type": [
            "The type field is required."
        ],
        "amount": [
            "The amount field is required."
        ]
    }
}
</code></pre>
{% endtab %}

{% tab title="201: Created " %}
```json
{
    // See Get product
}
```
{% endtab %}
{% endtabs %}

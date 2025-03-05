# Update product

<mark style="color:purple;">`PATCH`</mark> `https://rcur.app/api/v2/products/{id}`

#### Path Parameters

| Name                                   | Type   | Description           |
| -------------------------------------- | ------ | --------------------- |
| {id}<mark style="color:red;">\*</mark> | String | The ID of the product |

#### Request Body

| Name                     | Type              | Description                                                                                                                                                                         |
| ------------------------ | ----------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| name                     | String            | The name of the product                                                                                                                                                             |
| amount                   | Double            | The amount of the product. Example: `14.99`                                                                                                                                         |
| vat                      | Integer \| String | The VAT in percentage. If using an invoice integration, use the ID of the Get VAT response.                                                                                         |
| interval                 | String            | Only applicable if `type` is `subscription` Possible values: `months` `weeks` `days` `years`                                                                                        |
| interval\_value          | Integer           | Only applicable if `type` is `subscription` The quantity of the interval. For example, when `interval` is set to `months` and `interval_value` to `1` it will be a monthly product. |
| times                    | Integer           | Only applicable when `type` is `subscription` . When set to `null` or `0`, the product subscription will be continuously.                                                           |
| woocommerce\_product\_id | Integer           | Only applicable when WooCommerce integration enabled. The product ID or variation ID of the WooCommerce product.                                                                    |

{% tabs %}
{% tab title="200: OK " %}
```javascript
{
    // See Get product respons
}
```
{% endtab %}

{% tab title="422: Unprocessable Entity " %}
```json
{
    "status": 422,
    "error": "Could not update product. Some fields contain invalid data",
    "fields": {
        "amount": [
            "The amount must be a number."
        ]
    }
}
```
{% endtab %}
{% endtabs %}

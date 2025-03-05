# Delete product

<mark style="color:red;">`DELETE`</mark> `https://rcur.app/api/v2/products/{id}`

#### Path Parameters

| Name                                   | Type   | Description           |
| -------------------------------------- | ------ | --------------------- |
| {id}<mark style="color:red;">\*</mark> | String | The ID of the product |

{% tabs %}
{% tab title="404: Not Found " %}
```json
{
    "status": 404,
    "error": "Product not found"
}
```
{% endtab %}

{% tab title="204: No Content " %}

{% endtab %}
{% endtabs %}

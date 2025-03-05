# Delete customer

<mark style="color:red;">`DELETE`</mark> `https://rcur.app/api/v2/customers/{id}`

#### Path Parameters

| Name                                   | Type   | Description            |
| -------------------------------------- | ------ | ---------------------- |
| {id}<mark style="color:red;">\*</mark> | String | The ID of the customer |

{% tabs %}
{% tab title="204: No Content " %}

{% endtab %}

{% tab title="404: Not Found " %}
```javascript
{
    "status": 404,
    "error": "Customer not found"
}
```
{% endtab %}
{% endtabs %}

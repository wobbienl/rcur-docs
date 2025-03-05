# Revoke mandate

<mark style="color:red;">`DELETE`</mark> `https://rcur.app/api/v2/customers/{id}/{customerId}/mandates/{id}`

#### Path Parameters

<table><thead><tr><th width="204">Name</th><th>Type</th><th>Description</th></tr></thead><tbody><tr><td>{customerId}<mark style="color:red;">*</mark></td><td>String</td><td>The ID of the customer</td></tr><tr><td>{id}<mark style="color:red;">*</mark></td><td>String</td><td>The ID of the mandate</td></tr></tbody></table>

{% tabs %}
{% tab title="204: No Content" %}

{% endtab %}

{% tab title="404: Not found" %}
```json
{
    "status": 404,
    "error": "Mandate not found"
}
```
{% endtab %}
{% endtabs %}


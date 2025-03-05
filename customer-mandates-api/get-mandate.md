# Get mandate

<mark style="color:blue;">`GET`</mark> `https://rcur.app/api/v2/customers/{customerId}/mandates/{id}`

#### Path Parameters

<table><thead><tr><th width="204">Name</th><th>Type</th><th>Description</th></tr></thead><tbody><tr><td>{customerId}<mark style="color:red;">*</mark></td><td>String</td><td>The ID of the customer</td></tr><tr><td>{id}<mark style="color:red;">*</mark></td><td>String</td><td>The ID of the mandate</td></tr></tbody></table>



{% tabs %}
{% tab title="200: OK" %}
```json
{
    "id": "mdt_f8D2mMkVk",
    "method": "directdebit",
    "status": "valid",
    "custom_mandate_reference": null,
    "signature_date": "2024-03-27",
    "details": {
        "consumer_name": "John Doe",
        "consumer_account": "NL18RABO0123459876",
        "consumer_bic": "RABONL2U",
        "card_holder": null,
        "card_number": null,
        "card_expiry_date": null,
        "card_label": null,
        "card_fingerprint": null
    }
}
```


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

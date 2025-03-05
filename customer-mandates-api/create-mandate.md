# Create mandate

<mark style="color:green;">`POST`</mark> `https://rcur.app/api/v2/customers/{customerId}/mandates`

#### Path Parameters

| Name                                           | Type   | Description            |
| ---------------------------------------------- | ------ | ---------------------- |
| {customerId}<mark style="color:red;">\*</mark> | String | The ID of the customer |

#### Request Body

<table><thead><tr><th width="259">Name</th><th width="211">Type</th><th>Description</th></tr></thead><tbody><tr><td>consumer_name<mark style="color:red;">*</mark></td><td>String</td><td>The name of the account holder</td></tr><tr><td>consumer_account<mark style="color:red;">*</mark></td><td>String</td><td>The IBAN of the customer</td></tr><tr><td>custom_mandate_reference</td><td>String</td><td>A custom mandate reference. Leave it empty to let Mollie generate a unique reference</td></tr></tbody></table>

{% hint style="warning" %}
If you want to specify a custom mandate reference, make sure it is unique across **all Mollie customers** otherwise banks can reject the payments.
{% endhint %}

{% tabs %}
{% tab title="201: Created" %}
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

{% tab title="422: Unprocessable Entity " %}
```json
{
    "status": 422,
    "error": "Could not create mandate. Some fields contain invalid data",
    "fields": {
        "consumer_name": [
            "The consumer name field is required."
        ]
    }
}
```


{% endtab %}
{% endtabs %}


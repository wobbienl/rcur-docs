# List mandates

<mark style="color:blue;">`GET`</mark> `https://rcur.app/api/v2/customers/{customerId}/mandates`

#### Path Parameters

| Name                                           | Type   | Description            |
| ---------------------------------------------- | ------ | ---------------------- |
| {customerId}<mark style="color:red;">\*</mark> | String | The ID of the customer |



{% tabs %}
{% tab title="200: OK" %}
<pre class="language-json"><code class="lang-json"><strong>{
</strong>    "data": [
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
    ]
}
</code></pre>


{% endtab %}
{% endtabs %}

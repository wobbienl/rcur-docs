# Get payment

<mark style="color:blue;">`GET`</mark> `https://rcur.app/api/v2/payments/{id}`

#### Path Parameters

| Name                                   | Type   | Description                |
| -------------------------------------- | ------ | -------------------------- |
| {id}<mark style="color:red;">\*</mark> | String | The ID of the RCUR payment |

{% tabs %}
{% tab title="200: OK " %}
```json
{
    "id": "OBNJ3NAV8a",
    "mollie_payment_id": "tr_craNyczyz6",
    "mollie_payment_status": "paid",
    "webhook_url": null
}
```
{% endtab %}
{% endtabs %}

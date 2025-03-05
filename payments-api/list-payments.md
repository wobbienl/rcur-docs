# List payments

<mark style="color:blue;">`GET`</mark> `https://rcur.app/api/v2/payments`

{% tabs %}
{% tab title="200: OK " %}
```json
{
    "data": [
        {
            "id": "OBNJ3NAV8a",
            "mollie_payment_id": "tr_craNyczyz6",
            "mollie_payment_status": "paid",
            "webhook_url": null
        },
        {
            "id": "gm9Aml4b5B",
            "mollie_payment_id": "tr_craNyczyz4",
            "mollie_payment_status": "cancelled",
            "webhook_url": null
        },
        {
            "id": "xQjJ1xAe2P",
            "mollie_payment_id": "tr_craNyczyz5",
            "mollie_payment_status": "expired",
            "webhook_url": null
        },
        {
            "id": "RxDA7mzeLE",
            "mollie_payment_id": "tr_craNyczyz3",
            "mollie_payment_status": "paid",
            "webhook_url": null
        },
        {
            "id": "EZb4Exzlje",
            "mollie_payment_id": "tr_craNyczyz2",
            "mollie_payment_status": "paid",
            "webhook_url": "https://yourwebsite.com/rcur/webhook"
        }
    ]
}
```
{% endtab %}
{% endtabs %}

# Get subscription

<mark style="color:blue;">`GET`</mark> `https://rcur.app/api/v2/subscriptions/{id}`

#### Path Parameters

| Name                                   | Type   | Description                |
| -------------------------------------- | ------ | -------------------------- |
| {id}<mark style="color:red;">\*</mark> | String | The ID of the subscription |

{% tabs %}
{% tab title="200: OK " %}
```json
{
    "id": "DjqJBKQ4b7",
    "name": "Monthly Suprise box",
    "status": "active",
    "start_date": "2025-01-06",
    "mollie_mandate_id": "mdt_k239Fnf3n",
    "mollie_profile_id": "pfl_f9WnBF92X",
    "next_payment_at": "2025-02-06",
    "next_amount": 19.99,
    "last_payment_created_at": "2025-01-06 06:01:05",
    "resume_at": null,
    "cancel_at": null,
    "created_at": "2025-01-02 16:12:49",
    "rules": [
        {
            "id": "maJ3rGqMqz",
            "amount": 19.99,
            "currency": "EUR",
            "interval": "month",
            "interval_amount": 1,
            "day": 0,
            "times": null,
            "times_done": 1
        }
    ],
    "customer": {
        "id": "YJRQAMRQ6y",
        "number": "RC1234",
        "first_name": "John",
        "last_name": "Doe",
        "email": "jdoe@doeco.org",
        "phone": "+31612345678",
        "organization_name": "Doe Co.",
        "address": "Street name 123",
        "postal_code": "1234AB",
        "city": "City name",
        "country": "NL",
        "vat_number": "NL123456789B01",
        "locale": "nl",
        "mollie_customer_id": "cst_xDjnf3Kdx",
        "created_at": "2022-02-24 12:34:56"
    }
}
```
{% endtab %}

{% tab title="404: Not Found " %}
```json
{
    "status": 404,
    "error": "Subscription not found"
}
```
{% endtab %}
{% endtabs %}

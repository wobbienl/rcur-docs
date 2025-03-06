# Update follow-up

<mark style="color:purple;">`PATCH`</mark> `https://rcur.app/api/v2/follow-ups/{id}`

#### Path Parameters

| Name                                   | Type   | Description             |
| -------------------------------------- | ------ | ----------------------- |
| {id}<mark style="color:red;">\*</mark> | String | The ID of the follow-up |

#### Request Body

<table><thead><tr><th>Name</th><th width="238">Type</th><th>Description</th></tr></thead><tbody><tr><td>status</td><td>String</td><td>The status of the follow-up. Possible values: <code>pending</code> <code>failed</code> <code>solved</code></td></tr></tbody></table>

{% tabs %}
{% tab title="200: OK" %}
```json
{
    "id": "aWG6AjRqyE",
    "description": "Monthly Subscription",
    "type": "both",
    "status": "pending",
    "amount": "5.00",
    "currency": "EUR",
    "mollie_profile_id": "pfl_dcC93D3jf",
    "mollie_payment_id": "tr_fdfx2Fnf",
    "reason": null,
    "reason_code": "MD03",
    "retries_done": 1,
    "mails_sent": 2,
    "next_retry_at": "2025-03-07",
    "created_at": "2025-03-05 20:57:50",
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
    },
    "subscription": null,
    "order": null
}
```


{% endtab %}

{% tab title="404: Not Found" %}
```json
{
    "status": 404,
    "error": "Follow-up not found"
}
```


{% endtab %}
{% endtabs %}


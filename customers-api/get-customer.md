# Get customer

<mark style="color:blue;">`GET`</mark> `https://rcur.app/api/v2/customers/{id}`

#### Path Parameters

| Name                                   | Type   | Description            |
| -------------------------------------- | ------ | ---------------------- |
| {id}<mark style="color:red;">\*</mark> | String | The ID of the customer |

{% tabs %}
{% tab title="200: OK " %}
```json
{
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
```
{% endtab %}

{% tab title="404: Not Found " %}
```json
{
    "status": 404,
    "error": "Customer not found"
}
```
{% endtab %}
{% endtabs %}

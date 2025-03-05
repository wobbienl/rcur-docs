# List customers

<mark style="color:blue;">`GET`</mark> `https://rcur.app/api/v2/customers`

#### Query Parameters

<table><thead><tr><th width="219">Name</th><th>Type</th><th>Description</th></tr></thead><tbody><tr><td>page</td><td>Integer</td><td>Used for pagination. Default: 1</td></tr></tbody></table>

{% tabs %}
{% tab title="200: OK " %}
```json
{
    "data": [
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
        },
        ...
    ],
    "links": {
        "first": "https://rcur.app/api/v2/customers?page=1",
        "last": "https://rcur.app/api/v2/customers?page=2",
        "prev": null,
        "next": "https://rcur.app/api/v2/customers?page=2"
    },
    "meta": {
        "current_page": 1,
        "from": 1,
        "last_page": 2,
        "links": [
            {
                "url": null,
                "label": "&laquo; Previous",
                "active": false
            },
            {
                "url": "https://rcur.app/api/v2/customers?page=1",
                "label": "1",
                "active": true
            },
            {
                "url": "https://rcur.app/api/v2/customers?page=2",
                "label": "2",
                "active": false
            },
            {
                "url": "https://rcur.app/api/v2/customers?page=2",
                "label": "Next &raquo;",
                "active": false
            }
        ],
        "path": "https://rcur.app/api/v2/customers",
        "per_page": 15,
        "to": 15,
        "total": 29
    }
}
```
{% endtab %}
{% endtabs %}

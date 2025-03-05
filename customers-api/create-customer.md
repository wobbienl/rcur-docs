# Create customer

<mark style="color:green;">`POST`</mark> `https://rcur.app/api/v2/customers`

#### Request Body

| Name                                          | Type   | Description                                                                                                             |
| --------------------------------------------- | ------ | ----------------------------------------------------------------------------------------------------------------------- |
| first\_name<mark style="color:red;">\*</mark> | String | The first name of the customer                                                                                          |
| last\_name<mark style="color:red;">\*</mark>  | String | The last name of the customer                                                                                           |
| email<mark style="color:red;">\*</mark>       | String | The email address of the customer                                                                                       |
| number                                        | String | An internal number or reference of the customer                                                                         |
| phone                                         | String | The phone number of the customer                                                                                        |
| organization\_name                            | String | The organization name of the customer                                                                                   |
| address                                       | String | The address of the customer, incl. street number                                                                        |
| postal\_code                                  | String | The postal code of the customer                                                                                         |
| city                                          | String | The city of the customer's address                                                                                      |
| country                                       | String | The country of the customer's address in [ISO 3166-1 alpha-2](https://en.wikipedia.org/wiki/ISO_3166-1_alpha-2) format. |
| vat\_number                                   | String | The VAT number of the customer                                                                                          |
| locale                                        | String | The language of the customer. Possible options: `en` `nl` `de` `fr` `es`                                                |

{% tabs %}
{% tab title="201: Created " %}
```javascript
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

{% tab title="422: Unprocessable Entity " %}
```json
{
    "status": 422,
    "error": "Could not create customer. Some fields contain invalid data",
    "fields": {
        "first_name": [
            "The first name field is required."
        ],
        "email": [
            "The email must be a valid email address."
        ],
        "country": [
            "The country must be uppercase."
        ],
        "locale": [
            "The locale is invalid."
        ],
        "vat_number": [
            "The vat number is incorrect"
        ]
    }
}
```
{% endtab %}
{% endtabs %}

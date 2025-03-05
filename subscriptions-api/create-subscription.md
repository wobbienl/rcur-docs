# Create subscription

<mark style="color:green;">`POST`</mark> `https://rcur.app/api/v2/subscriptions`

#### Request Body

| Name                                                  | Type              | Description                                                                            |
| ----------------------------------------------------- | ----------------- | -------------------------------------------------------------------------------------- |
| name<mark style="color:red;">\*</mark>                | String            | The name of the subscription                                                           |
| customer\_id<mark style="color:red;">\*</mark>        | String            | The ID of the customer                                                                 |
| mollie\_profile\_id<mark style="color:red;">\*</mark> | String            | The ID of the Mollie profile                                                           |
| mollie\_mandate\_id<mark style="color:red;">\*</mark> | String            | The ID of the Mollie customer mandate                                                  |
| start\_date<mark style="color:red;">\*</mark>         | Date (yyyy-mm-dd) | The start date of the subscription. Must be equal to or after today                    |
| workflow\_id                                          | Integer           | The workflow ID of Moneybird. Required if the Moneybird invoice integration is enabled |
| docstyle\_id                                          | Integer           | The docstyle ID of Moneybird. Required if the Moneybird invoice integration is enabled |
| rules<mark style="color:red;">\*</mark>               | Array             | The rules of the subscription                                                          |

#### Rules object

| Name                                               | Type    | Description                                                                                          |
| -------------------------------------------------- | ------- | ---------------------------------------------------------------------------------------------------- |
| amount<mark style="color:red;">\*</mark>           | Amount  | The amount of the rule in EUR. Not required if an invoice integration is active                      |
| interval<mark style="color:red;">\*</mark>         | String  | The interval of the rule. Possible options: `day` `week` `month` `year`                              |
| interval\_amount<mark style="color:red;">\*</mark> | Integer | The interval amount of the rule. Minimum amount: 1                                                   |
| day<mark style="color:red;">\*</mark>              | Integer | The day of charging the rule. Value depends on the chosen interval. `0` is the day of the start date |
| times                                              | Integer | The number of times a rule will charge the customer. Leave out for an ongoing rule                   |
| invoice\_rules                                     | Array   | The invoice rules of the subscription rule. Required if an invoice integration is enabled            |

#### Invoice rules object

| Name                                          | Type              | Description                                                                                  |
| --------------------------------------------- | ----------------- | -------------------------------------------------------------------------------------------- |
| quantity<mark style="color:red;">\*</mark>    | Integer           | The quantity of the invoice rule                                                             |
| description<mark style="color:red;">\*</mark> | String            | The description of the invoice rule                                                          |
| amount<mark style="color:red;">\*</mark>      | Amount            | The amount of the invoice rule of a single quantity                                          |
| vat<mark style="color:red;">\*</mark>         | String or Integer | The VAT of the invoice rule. Type depends on the invoice integration                         |
| ledger\_account\_id                           | String            | The ledger account ID of Moneybird. Required if the Moneybird invoice integration is enabled |

{% tabs %}
{% tab title="201: Created " %}
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

{% tab title="422: Unprocessable Entity " %}
```json
{
    "status": 422,
    "error": "Could not create subscription. Some fields contain invalid data",
    "fields": {
        "name": [
            "The name field is required."
        ]
    }
}
```
{% endtab %}
{% endtabs %}

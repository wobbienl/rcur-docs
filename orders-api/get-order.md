# Get order

<mark style="color:blue;">`GET`</mark> `https://rcur.app/api/v2/orders/{id}`

#### Path Parameters

| Name                                   | Type   | Description         |
| -------------------------------------- | ------ | ------------------- |
| {id}<mark style="color:red;">\*</mark> | String | The ID of the order |

{% tabs %}
{% tab title="200: OK " %}
<pre class="language-json"><code class="lang-json">{
    "id": "pw9vVbv1ko",
    "order_number": 100001,
    "status": "completed",
    "first_name": "John",
    "last_name": "Doe",
    "email": "jdoe@doeco.org",
    "organization_name": "Doe Co.",
    "phone": "+31612345678",
    "address": "Street name 123",
    "postal_code": "1234AB",
    "city": "City name",
    "country": "NL",
    "vat_number": "NL12345678B01",
    "carrier": "postnl",
    "tracktrace": "3S1234567890",
    "wc_order_id": 12345,
    "wc_order_number": "ORD-12345",
    "subscription": true,
    "subscription_status": "<a data-footnote-ref href="#user-content-fn-1">cancelled</a>",
    "cancel_subscription_at": "2023-02-12",
    "total_amount": "6.00",
    "currency": "EUR",
    "created_at": "2023-02-08 14:36:33",
    "products": [
        {
            "next_order": null,
            "quantity": 1,
            "product": {
                // See Get product
            }
        },
        {
            "next_order": "2023-03-08",
            "quantity": 1,
            "product": {
                // See Get product
            }
        }
    ],
    "customer": {
        // See Get customer
    },
    "parent": {
        // See Get order
    }
}
</code></pre>
{% endtab %}

{% tab title="404: Not Found " %}
```json
{
    "status": 404,
    "error": "Order not found"
}
```
{% endtab %}
{% endtabs %}

[^1]: Possible values: `active` `cancelled` `completed`

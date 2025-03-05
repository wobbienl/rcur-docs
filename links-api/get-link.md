# Get link

<mark style="color:blue;">`GET`</mark> `https://rcur.app/api/v2/link/{id}`

#### Path Parameters

| Name                                   | Type   | Description        |
| -------------------------------------- | ------ | ------------------ |
| {id}<mark style="color:red;">\*</mark> | String | The ID of the link |

{% tabs %}
{% tab title="200: OK" %}
```json
{
    "id": "nMvOMqXgxP",
    "status": "open",
    "active": true,
    "type": "payment",
    "description": "Test",
    "currency": "EUR",
    "amount": "5.00",
    "first_amount": null,
    "interval": null,
    "times": null,
    "trial_interval": null,
    "reminder_at": null,
    "redirect_url_paid": null,
    "redirect_url_failed": null,
    "expires_at": null,
    "created_at": "2020-04-20 20:30:11",
    "url": "https://rcur.app/pay/nMvOMqXgxP",
}
```
{% endtab %}

{% tab title="404: Not Found" %}
```json
{
    "status": 404,
    "error": "Link not found"
}
```
{% endtab %}
{% endtabs %}


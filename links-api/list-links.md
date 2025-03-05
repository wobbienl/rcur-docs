# List links

<mark style="color:blue;">`GET`</mark> `https://rcur.app/api/v2/links`

#### Query Parameters

<table><thead><tr><th width="219">Name</th><th>Type</th><th>Description</th></tr></thead><tbody><tr><td>page</td><td>Integer</td><td>Used for pagination. Default: 1</td></tr></tbody></table>

{% tabs %}
{% tab title="200: OK" %}
```json
{
    "data": [
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
            "created_at": "2020-04-20 20:30:11"
            "url": "https://rcur.app/pay/nMvOMqXgxP",
        }
    ],
    "links": {
        "first": "https://rcur.app/api/v2/links?page=1",
        "last": "https://rcur.app/api/v2/links?page=2",
        "prev": null,
        "next": "https://rcur.app/api/v2/links?page=2"
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
                "url": "https://rcur.app/api/v2/links?page=1",
                "label": "1",
                "active": true
            },
            {
                "url": "https://rcur.app/api/v2/links?page=2",
                "label": "2",
                "active": false
            },
            {
                "url": "https://rcur.app/api/v2/links?page=2",
                "label": "Next &raquo;",
                "active": false
            }
        ],
        "path": "https://rcur.app/api/v2/links",
        "per_page": 15,
        "to": 15,
        "total": 26
    }
}
```
{% endtab %}
{% endtabs %}


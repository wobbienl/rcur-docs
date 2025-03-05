# List orders

<mark style="color:blue;">`GET`</mark> `https://rcur.app/api/v2/orders`

#### Query Parameters

| Name | Type    | Description                     |
| ---- | ------- | ------------------------------- |
| page | Integer | Used for pagination. Default: 1 |

{% tabs %}
{% tab title="200: OK " %}
```json
{
    "data": [
        {
            "id": "s8K230mEd",
            ... // See Get order
        },
        {
            ...
        }
    ],
    "links": {
        "first": "https://rcur.app/api/v2/orders?page=1",
        "last": "https://rcur.app/api/v2/orders?page=1",
        "prev": null,
        "next": null
    },
    "meta": {
        "current_page": 1,
        "from": 1,
        "last_page": 1,
        "links": [
            {
                "url": null,
                "label": "&laquo; Previous",
                "active": false
            },
            {
                "url": "https://rcur.app/api/v2/orders?page=1",
                "label": "1",
                "active": true
            },
            {
                "url": null,
                "label": "Next &raquo;",
                "active": false
            }
        ],
        "path": "https://rcur.app/api/v2/orders",
        "per_page": 15,
        "to": 1,
        "total": 1
    }
}
```
{% endtab %}
{% endtabs %}

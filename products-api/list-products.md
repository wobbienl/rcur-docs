# List products

<mark style="color:blue;">`GET`</mark> `https://rcur.app/api/v2/products`

#### Query Parameters

| Name | Type    | Description                     |
| ---- | ------- | ------------------------------- |
| page | Integer | Used for pagination. Default: 1 |

{% tabs %}
{% tab title="200: OK " %}
```javascript
{
    "data": [
        {
            "id": "eK9g8GXMY0",
            ... // See Get product
        },
        ...
    ],
    "links": {
        "first": "https://rcur.app/api/v2/products?page=1",
        "last": "https://rcur.app/api/v2/products?page=1",
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
                "url": "https://rcur.app/api/v2/products?page=1",
                "label": "1",
                "active": true
            },
            {
                "url": null,
                "label": "Next &raquo;",
                "active": false
            }
        ],
        "path": "https://rcur.app/api/v2/products",
        "per_page": 15,
        "to": 2,
        "total": 2
    }
}
```
{% endtab %}
{% endtabs %}

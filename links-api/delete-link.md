# Delete link

<mark style="color:red;">`DELETE`</mark> `https://rcur.app/api/v2/links/{id}`

#### Path Parameters

| Name                                   | Type   | Description        |
| -------------------------------------- | ------ | ------------------ |
| {id}<mark style="color:red;">\*</mark> | String | The ID of the link |

{% tabs %}
{% tab title="204: No Content" %}

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


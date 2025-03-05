# Authentication

To use our API, you'll need to generate an API key in your RCUR account. You can do this on the [integrations page](https://rcur.app/app/settings/integrations).

The API key must be sent along with each API request, by providing it in the HTTP call’s `Authorization` header using the `Bearer` method. For example: a valid `Authorization` header is `Bearer xsDOtmnkVtjNVWXLSlXsM`

In the example below we use an API key on the `GET` method of the `customers` resource. This method fetches a customer.

```bash
curl -X GET https://rcur.app/api/v2/customers/YJRQAMRQ6y \
    -H "Authorization: Bearer xsDOtmnkVtjNVWXLSlXsM"
```


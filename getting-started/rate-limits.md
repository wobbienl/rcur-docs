# Rate limits

Currently, the rate limit is 60 request per minute.

### Checking the status of your rate limit <a href="#checking-the-status-of-your-rate-limit" id="checking-the-status-of-your-rate-limit"></a>

You can use the headers that are sent with each response to determine the current status of your primary rate limit.

| Header name           | Description                                                                  |
| --------------------- | ---------------------------------------------------------------------------- |
| x-ratelimit-limit     | The maximum number of requests that you can make per hour                    |
| x-ratelimit-remaining | The number of requests remaining in the current rate limit window            |
| x-ratelimit-reset     | The time at which the current rate limit window resets, in UTC epoch seconds |
| retry-after           | The number of seconds you have to wait before you can make new requests      |


# Client caching

A sample Ktor project showing how to use the [HttpCache](https://ktor.io/docs/client-caching.html) plugin.

## Running

Before running this sample, start a server from the [caching-headers](../caching-headers) example:
```bash
./gradlew :caching-headers:run
```

This sample has the `/customer/1` route that responds with a JSON object with the configured `Cache-Control` header.

To see the client's caching in action, run this example by executing the following command:

```bash
./gradlew :client-caching:run
```

The client will cache the result of the first `GET` request and won't send a second request.

> Note that this example uses the [Logging](https://ktor.io/docs/client-logging.html) plugin to show a request in a console.
## Cooperator Developer Experience

* As part of the service's CI we can then add in a client library using `OpenAPI-Generator` (this can be in python, java, typescript etc.)
  * The said client library will be generated as part of the API's CI see [Diagram](./diagrams.md#ci--cd-service).

By doing the above, it will give us a guarantee that the API that the Client (Cooperator) uses is in sync with the latest API from the service, another thing to note, that on the endpoint `rest/<VERSION>/....` the `<VERSION>` in the endpoint is using the Major Version and the equivalent Library version should always match the Major Version (Irrespective of the Minor/Patch version).

eg:, `/rest/v1/reservation` and the equivalent version of the client lib(s) to use is `v1.0.0` or `v1.1.0` etc.

<hr/>

[back](./README.md)

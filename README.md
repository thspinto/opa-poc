# OPA PoC

This is a Poc to test OPA integration with APIs.

## Use cases

* Keycloak as IdP
* Kong as API gateway
* Generating policies and integration with spring boot
* Auditing using ES
* Policy testing and authorization replay

## Running

Spin up everything with:

```bash
docker-compose up -d
```

Testing:

```
curl --user david:password localhost:8000/finance/salary/alice
curl --user david:password localhost:8000/finance/salary/bob
curl --user david:password localhost:8000/finance/salary/charlie
curl --user david:password localhost:8000/finance/salary/david
```

Decision logs should be available in [Kibana](http://localhost:5601/)

## References

* [Microserices example](https://github.com/open-policy-agent/opa/blob/master/docs/content/http-api-authorization.md)
* [Microservices with OPA](https://medium.com/@KevinHoffman/securing-microservices-with-open-policy-agent-fcf04d982b4a)
* [Kong docker compose](https://github.com/Kong/docker-kong/tree/master/compose)

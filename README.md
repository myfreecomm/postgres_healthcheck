When working with containers it is often necessary to need a service to be up and running before the application itself. This is specially true in CI environments, where you can't just spin up the application again.

This Postgres image, [basically the same as healthcheck/postgres](https://github.com/docker-library/healthcheck/tree/master/postgres),
leverages the [`HEALTHCHECK`](https://docs.docker.com/engine/reference/builder/#healthcheck) directive.

The only difference between this and the oficial _healtcheck_ image is that we specify a version for Postgres instead of relying on `latest`.

# py-pkg-build-example

A simple demo package.

## Local development in Docker

Build docker image:
```sh
docker build \
    --no-cache \
    --platform=linux/amd64 \
    --tag py-pkg-build-example:latest \
    .
```

Run build:
```sh
docker run --platform=linux/amd64 py-pkg-build-example:latest
```

Interactive development:
```sh
docker run -it --rm \
    --volume .:/app \
    --volume /app/.venv \
    --platform=linux/amd64 \
    py-pkg-build-example:latest \
    /bin/bash
```
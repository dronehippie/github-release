# github-release

[![Current Tag](https://img.shields.io/github/v/tag/dronehippie/github-release?sort=semver)](https://github.com/dronehippie/github-release) [![Build Status](http://drone.webhippie.de/api/badges/dronehippie/github-release/status.svg)](http://drone.webhippie.de/api/badges/dronehippie/github-release) [![Join the Matrix chat at https://matrix.to/#/#webhippie:matrix.org](https://img.shields.io/badge/matrix-%23webhippie-7bc9a4.svg)](https://matrix.to/#/#webhippie:matrix.org) [![Docker Size](https://img.shields.io/docker/image-size/dronehippie/github-release/latest)](https://hub.docker.com/r/dronehippie/github-release) [![Docker Pulls](https://img.shields.io/docker/pulls/dronehippie/github-release)](https://hub.docker.com/r/dronehippie/github-release) [![Go Reference](https://pkg.go.dev/badge/github.com/dronehippie/github-release.svg)](https://pkg.go.dev/github.com/dronehippie/github-release) [![Go Report Card](https://goreportcard.com/badge/github.com/dronehippie/github-release)](https://goreportcard.com/report/github.com/dronehippie/github-release) [![Codacy Badge](https://app.codacy.com/project/badge/Grade/9e23d1db620a4063a030d37e1ec93bef)](https://www.codacy.com/gh/dronehippie/github-release/dashboard?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=dronehippie/github-release&amp;utm_campaign=Badge_Grade)

Drone plugin to upload build artifacts to GitHub releases. For the usage information and a listing of the available options please take a look at the [documentation](https://dronehippie.github.io/github-release/).

## Build

Build the binary with the following command:

```console
export GOOS=linux
export GOARCH=amd64

make build
```

## Docker

Build the image with the following command:

```console
docker build \
  --label org.opencontainers.image.source=https://github.com/dronehippie/github-release \
  --label org.opencontainers.image.revision=$(git rev-parse --short HEAD) \
  --label org.opencontainers.image.created=$(date -u +"%Y-%m-%dT%H:%M:%SZ") \
  --file docker/Dockerfile.amd64 --tag dronehippie/github-release .
```

## Usage

```console
docker run --rm \
  -e PLUGIN_DUMMY="dummy" \
  -v $(pwd):$(pwd) \
  -w $(pwd) \
  dronehippie/github-release
```

## Security

If you find a security issue please contact [thomas@webhippie.de](mailto:thomas@webhippie.de) first.

## Contributing

Fork -> Patch -> Push -> Pull Request

## Authors

-   [Thomas Boerger](https://github.com/tboerger)

## License

Apache-2.0

## Copyright

```console
Copyright (c) 2021 Thomas Boerger <thomas@webhippie.de>
```

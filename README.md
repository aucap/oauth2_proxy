# OAuth2 Proxy

[![Build Status](https://travis-ci.com/rustyx/oauth2_proxy.svg?branch=dev)](https://travis-ci.com/rustyx/oauth2_proxy)

A reverse proxy and static file server that provides authentication using Providers (Google, GitHub, and others)
to validate accounts by email, domain or group.

**Note:** This repository is a fork of [oauth2-proxy/oauth2-proxy](https://github.com/oauth2-proxy/oauth2-proxy) that adds the subdomain routing feature, which is configurable in the [Upstream Configuration](https://github.com/rustyx/oauth2_proxy/blob/dev/docs/configuration/configuration.md#upstreams-configuration).

```
test |http://127.0.0.1:8082/
other|http://127.0.0.1:8083/
other|http://127.0.0.1:8084/path/
     |http://127.0.0.1:8085/
```

A list of changes can be seen in the [CHANGELOG](CHANGELOG.md).

![Sign In Page](https://cloud.githubusercontent.com/assets/45028/4970624/7feb7dd8-6886-11e4-93e0-c9904af44ea8.png)

## Installation

1.  Choose how to deploy:

    a. Build with `go get github.com/rustyx/oauth2_proxy` which will put the binary in `$GOROOT/bin`

    b. Using the prebuilt docker image [rustyx/oauth2_proxy](https://hub.docker.com/repository/docker/rustyx/oauth2_proxy) (Linux AMD64)

2.  [Select a Provider and Register an OAuth Application with a Provider](https://github.com/rustyx/oauth2_proxy/blob/dev/docs/2_auth.md)
3.  [Configure OAuth2 Proxy using config file, command line options, or environment variables](https://github.com/rustyx/oauth2_proxy/blob/dev/docs/configuration/configuration.md)
4.  [Configure SSL or Deploy behind a SSL endpoint](https://github.com/rustyx/oauth2_proxy/blob/dev/docs/4_tls.md) (example provided for Nginx)


## Security

If you are running a version older than v5.0.0 we **strongly recommend you please update** to a current version. RE: [open redirect vulnverability](https://github.com/oauth2-proxy/oauth2-proxy/security/advisories/GHSA-qqxw-m5fj-f7gv)

## Docs

![OAuth2 Proxy Architecture](https://cloud.githubusercontent.com/assets/45028/8027702/bd040b7a-0d6a-11e5-85b9-f8d953d04f39.png)

[Configuration](https://github.com/rustyx/oauth2_proxy/blob/dev/docs/configuration/configuration.md)

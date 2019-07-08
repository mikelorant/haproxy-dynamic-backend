# haproxy-dynamic-backend

## Overview

Proof of concept of a dynamic backend for HAProxy. This is useful when it is not desireable to use an IP address for the backend as it is likely to change.

## Usage

Basic example that proxies all requests to Google.
```
docker-compose up -d
docker-comport port haproxy 8080
```

## Configuration

All configuration is done as enviromental variables.

| NAME           | DEFAULT            | DESCRIPTION                      |
| -------------- | ------------------ | -------------------------------- |
| DNS_SERVER     | 8.8.8.8            | DNS server to use as a resolver. |
| BIND_PORT      | 8080               | Frontend port to listen to.      |
| BACKEND_SERVER | www.google.com:443 | Backend hostname and port.       |
| HOST_HEADER    | www.google.com     | Host header to send.             |
| CACHE_SIZE     | 100                | Cache size in megabytes.         |


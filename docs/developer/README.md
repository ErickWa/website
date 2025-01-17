---
title: 'API and client library documentation'
---

# Developer

This section helps developers build applications that use drand as a source of randomness. For help running your own drand network, see the [Operator's Guide](/operator/).

The current public League of Entropy drand mainnet API endpoints are:

* `https://api.drand.sh` (HTTPS endpoint, also available over HTTP)
* `https://api2.drand.sh` (HTTPS endpoint, also available over HTTP)
* `https://api3.drand.sh` (HTTPS endpoint, also available over HTTP)
* `https://drand.cloudflare.com` (HTTPS endpoint)
* `https://api.drand.secureweb3.com:6875` (HTTPS endpoint)
* `/dnsaddr/api.drand.sh` (1st-level libp2p gossipsub relay endpoint)
* `/dnsaddr/api2.drand.sh` (1st-level libp2p gossipsub relay endpoint)
* `/dnsaddr/api3.drand.sh` (1st-level libp2p gossipsub relay endpoint)

There are two networks on mainnet:
- `default` which is running the chained scheme with public keys on G1
- `fastnet` which is running the unchained scheme with public keys on G2

`default` network chain hash: 
```8990e7a9aaed2ffed73dbd7092123d6f289930540d7651336225dc172e51b2ce```

`fastnet` network chain hash: 
```dbd506d6ef76e5f386f41c651dcb808c5bcbd75471cc4eafa3f4df7ad4e4c493```

In order to retrieve randomness from a drand network you should **preferentially use the [drand client libraries](/developer/clients/) or the [drand-client CLI](/developer/drand-client/)**, which support the different mechanisms and perform verification for every value obtained.

Alternatively, you can interact directly with the endpoints. Make sure to manually verify every value:

- [HTTP API reference](/developer/http-api/)
- [Pubsub-based randomness distribution](/developer/gossipsub/)
- gRPC API: usually not publicly accessible. A gRPC API is supported by the drand client libraries, the `drand-client` CLI application and the [drand application](/operator/drand-cli/) itself (using `drand get public`).

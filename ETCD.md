# ETCD

## Register services

```
curl -L http://127.0.0.1:4001/v2/keys/services/myservice -XPUT -d value="http://foo" -d ttl=5
```

## Service Health

Values are stored with a Time To Live.
Services needs to refresh this TTL for the service to appear healthy

## DNS

SkyDNS is a thin layer on top of ETCD providing DNS resolution.
https://github.com/skynetservices/skydns

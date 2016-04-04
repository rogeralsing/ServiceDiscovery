# ETCD

## Register services

```
curl -L http://127.0.0.1:4001/v2/keys/services/myservice/serviceid -XPUT -d value="http://foo" -d ttl=5
```

* `services` this part of the URI could be anything, it is just the path that you want to use.
* `myservice` this is the name of the service you want to register
* `serviceid` this is a unique id for the specific service instance you want to register.

## Service Health

Values are stored with a Time To Live.
Services needs to refresh this TTL for the service to appear healthy

## DNS support

SkyDNS is a thin layer on top of ETCD providing DNS resolution.
https://github.com/skynetservices/skydns

# Squid with Basic Auth

Repo based on https://github.com/sameersbn/docker-squid#configuration

It just adds a simple configuration file and a password file, which can be useful for local testing.

How to run the proxy:

```
docker run --rm --name squid --publish 3128:3128 -v ${PWD}/squid.conf:/etc/squid/squid.conf \
  -v ${PWD}/squid/cache:/var/spool/squid -v ${PWD}/passwords:/etc/squid/passwords sameersbn/squid:3.5.27
```

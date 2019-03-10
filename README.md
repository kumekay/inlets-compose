# inlets-compose

Docker Compose Config for Inlets (behind Traefik as reverse proxy)

in `docker-compose.yml` replace `[example.com]` and `[your token]` with your token, you can generate one with `head -c 16 /dev/urandom | shasum | cut -d\" \" -f1`

Then to expose local port run, say 8000:

```
inlets -server=false -upstream=http://127.0.0.1:8000 -remote=wss://[example.com] -token=[token]
```

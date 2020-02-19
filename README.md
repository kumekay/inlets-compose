# inlets-compose

Docker Compose Config for Inlets (behind Traefik as reverse proxy)

Create `.env` file (`cp .env.sample .env`) and replace `example.com` with your domain and `super_secret_token` with your token, you can generate one with `head -c 16 /dev/urandom | shasum | cut -d' ' -f1`

Then to expose local port run, say 8000:

```
inlets client --upstream=http://127.0.0.1:8000 --remote=wss://[example.com] --token=[token]
```

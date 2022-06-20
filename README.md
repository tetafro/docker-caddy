# Info

Docker image with Caddy web server installed. Based on lib/alpine.

## Run with custom config

Put caddy configuration file in a separate directory and run
```sh
docker run -d \
    -p 80:80 \
    -p 443:443 \
    -v $(pwd)/conf:/srv \
   ghcr.io/tetafro/caddy -conf /srv/Caddyfile
```

## Available versions

| Tag     | Info
| ------- | ---
| v0.11.4 | Caddy 0.11.4 based on Alpine Linux 3.8
| v1.0.3  | Caddy 1.0.3 based on Alpine Linux 3.10

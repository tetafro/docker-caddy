# Info

Docker image with Caddy web server installed. Based on lib/alpine.

This image is available on [Docker Hub](https://hub.docker.com/r/tetafro/caddy/).

## Run with custom config

Put caddy configuration file in a separate directory and run
```sh
docker run -d \
    -p 80:80 \
    -p 443:443 \
    -v $(pwd)/conf:/srv \
    tetafro/caddy -conf /srv/Caddyfile
```

## Available versions

| Tag    | Info
| ------ | ---
| 0.11.4 | Caddy 0.11.4 based on Alpine Linux 3.8
| latest | Same as 0.11.4

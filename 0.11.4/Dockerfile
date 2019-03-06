FROM alpine:3.8 AS build

ENV VERSION=0.11.4

RUN apk add --no-cache curl ca-certificates && \
    curl -sL https://github.com/mholt/caddy/releases/download/v${VERSION}/caddy_v${VERSION}_linux_amd64.tar.gz | tar xz

FROM alpine:3.8

RUN apk add --no-cache ca-certificates

COPY --from=build /caddy /usr/local/bin/caddy

EXPOSE 80 443 2015

ENTRYPOINT ["caddy"]

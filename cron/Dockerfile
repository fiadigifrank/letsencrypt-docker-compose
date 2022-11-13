FROM alpine:latest

RUN apk update && apk add --no-cache sh docker-cli docker-cli-compose

COPY renew_certs.sh /etc/periodic/daily/renew_certs

RUN chmod +x /etc/periodic/daily/renew_certs

WORKDIR /workdir

CMD ["crond", "-f", "-l", "0"]

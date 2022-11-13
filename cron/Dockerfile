FROM arm64v8/alpine

RUN apk update \
apk upgrade \
apk add --no-cache bash \
bash-doc \
bash-completion \
rm -rf /var/cache/apk/* \
/bin/sh 
&& apk add --no-cache docker-cli docker-cli-compose

COPY renew_certs.sh /etc/periodic/daily/renew_certs

RUN chmod +x /etc/periodic/daily/renew_certs

WORKDIR /workdir

CMD ["crond", "-f", "-l", "0"]

FROM certbot/certbot:arm64v8-latest
FROM certbot/certbot:latest

RUN apk add --no-cache bash

COPY certbot.sh /opt/

RUN chmod +x /opt/certbot.sh

ENV PATH=/usr/local/bin:$PATH

ENTRYPOINT ["/opt/certbot.sh"]

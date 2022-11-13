FROM certbot/certbot:latest

RUN apk add --no-cache sh

COPY certbot.sh /opt/

RUN chmod +x /opt/certbot.sh

ENTRYPOINT ["/opt/certbot.sh"]

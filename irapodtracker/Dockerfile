FROM alpine:latest

WORKDIR /usr/local/bin/

COPY irapodtracker /usr/local/bin/irapodtracker

RUN chmod +x /usr/local/bin/irapodtracker

RUN mkdir -p /usr/local/epi/conf

CMD ["/usr/local/epi/irapodtracker"]


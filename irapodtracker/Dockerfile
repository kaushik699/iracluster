FROM alpine:latest

WORKDIR /usr/local/bin/

COPY IraPodTracker /usr/local/bin/IraPodTracker

RUN chmod +x /usr/local/bin/IraPodTracker

RUN mkdir -p /usr/local/epi/conf

CMD ["/usr/local/epi/irapodtracker"]


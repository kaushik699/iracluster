FROM alpine:latest

WORKDIR /usr/local/bin/

COPY IraPodWatcher /usr/local/bin/

RUN chmod +x /usr/local/bin/IraPodWatcher

RUN mkdir -p /usr/local/epi/conf

CMD ["/usr/local/bin/IraPodWatcher"]


FROM alpine:latest

WORKDIR /usr/local/bin/

COPY IraPodWatcher /usr/local/bin/IraPodWatcher

RUN chmod +x /usr/local/bin/IraPodWatcher

RUN mkdir -p /usr/local/bin/conf

CMD ["/usr/local/bin/IraPodWatcher"]


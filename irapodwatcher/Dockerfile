FROM alpine:latest

WORKDIR /usr/local/epi/

COPY IraPodWatcher /usr/local/epi/IraPodWatcher

RUN chmod +x /usr/local/epi/IraPodWatcher

RUN mkdir -p /usr/local/epi/conf

CMD ["/usr/local/bin/IraPodWatcher"]


FROM ubuntu:22.04

RUN apt-get update

RUN apt-get install -y fortune cowsay

COPY entrypoint.sh /tmp/entrypoint.sh

RUN chmod 755 /tmp/entrypoint.sh

ENTRYPOINT /tmp/entrypoint.sh

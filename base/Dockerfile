FROM ubuntu:xenial as builder
MAINTAINER NlaakStudiosLLC

ENV DEBIAN_FRONTEND noninteractive

RUN apt-get update \
        && apt-get upgrade -q -y \
        && apt-get dist-upgrade -q -y \
        && apt-get install -q -y wget curl \
        && apt-get clean \
        && rm -rf /var/lib/apt/lists/* \
        && cd /tmp \
        && wget https://www.multichain.com/download/multichain-2.0-beta-2.tar.gz \
        && tar -xvzf multichain-2.0-beta-2.tar.gz

FROM scratch
COPY --from=builder /tmp/multichain-2.0-beta-2 /usr/local/bin
FROM debian:buster-slim

ARG JITSI_RELEASE=stable

ADD https://download.jitsi.org/jitsi-key.gpg.key /tmp/jitsi.key

RUN apt-get update && \
    apt-get upgrade --assume-yes && \
    apt-get install --no-install-recommends --assume-yes apt-transport-https apt-utils ca-certificates gnupg && \
    apt-key add /tmp/jitsi.key && \
    rm -f /tmp/jitsi.key && \
    echo "deb https://download.jitsi.org $JITSI_RELEASE/" > /etc/apt/sources.list.d/jitsi.list && \
    apt-get clean

FROM debian:jessie

RUN DEBIAN_FRONTEND=noninteractive apt-get update
RUN DEBIAN_FRONTEND=noninteractive apt-get install -y wget

RUN wget -O /tmp/bitcoin.tgz https://bitcoin.org/bin/bitcoin-core-0.12.1/bitcoin-0.12.1-linux64.tar.gz
RUN tar xvf /tmp/bitcoin.tgz -C /tmp/

RUN mkdir -p /srv/bitcoin-data; ln -s /srv/bitcoin-data /root/.bitcoin
RUN install -m 0755 -o root -g root -t /usr/local/bin/ /tmp/bitcoin-0.12.1/bin/*

VOLUME /srv/bitcoin-data/

EXPOSE 8332
EXPOSE 8333

USER nobody

CMD [ "bitcoind", "-datadir=/srv/bitcoin-data", "-printtoconsole"]

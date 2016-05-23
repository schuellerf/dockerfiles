FROM markusk/buildessentials

ARG DEBIAN_FRONTEND=noninteractive
RUN apt-get update && \
    apt-get install -y cmake apache2-dev libapr1-dev && \
    apt-get clean

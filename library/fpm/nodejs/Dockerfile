FROM ruby:slim
MAINTAINER Containerly <https://github.com/containerly>

RUN apt-get update && \
    apt-get upgrade -y && \
    apt-get install -y build-essential && \
    rm -rf /var/cache/apt/archives && \
    gem install --no-ri --no-rdoc fpm

WORKDIR /build
ENTRYPOINT ["/usr/local/bundle/bin/fpm"]
CMD ["--help"]

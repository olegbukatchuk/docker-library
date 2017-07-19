FROM fedora:latest
MAINTAINER Containerly <https://github.com/containerly>

RUN dnf makecache && \
    dnf upgrade -y && \
    dnf install -y ruby-devel gcc make rpm-build libffi-devel && \
    dnf clean all && \
    gem install --no-ri --no-rdoc fpm

WORKDIR /build
ENTRYPOINT ["/usr/local/bin/fpm"]

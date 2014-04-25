FROM ubuntu:12.04
ENV DEBIAN_FRONTEND noninteractive
RUN apt-get update -qq && apt-get install -y make curl -qq

ADD https://github.com/postmodern/ruby-install/archive/v0.4.0.tar.gz /tmp/
RUN cd /tmp && tar -zxvf v0.4.0.tar.gz
WORKDIR /tmp/ruby-install-0.4.0
RUN cd /tmp/ruby-install-0.4.0 && make install
WORKDIR /

ONBUILD RUN apt-get clean
ONBUILD ENTRYPOINT ["/bin/bash"]

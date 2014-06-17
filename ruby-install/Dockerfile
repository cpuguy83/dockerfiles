FROM ubuntu:14.04
ENV DEBIAN_FRONTEND noninteractive
ENV LANG en_US.UTF-8
ENV LANGUAGE en_US.UTF-8
ENV LC_ALL en_US.UTF-8

RUN apt-get update -qq && apt-get install -y make curl -qq && apt-get clean

ADD https://github.com/postmodern/ruby-install/archive/v0.4.3.tar.gz /tmp/
RUN cd /tmp && tar -zxvf v0.4.3.tar.gz && cd /tmp/ruby-install-0.4.3 && make install

ONBUILD ENTRYPOINT ["/bin/bash"]

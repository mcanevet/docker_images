FROM debian:wheezy

MAINTAINER mickael.canevet@camptocamp.com

ENV PUPPETSERVER_VERSION 2.1.1-1puppetlabs1

RUN apt-get update \
  && apt-get install -y curl \
  && curl -O http://apt.puppetlabs.com/puppetlabs-release-pc1-wheezy.deb \
  && dpkg -i puppetlabs-release-pc1-wheezy.deb \
  && apt-get update \
  && apt-get install -y puppetserver=$PUPPETSERVER_VERSION

ENTRYPOINT ["/opt/puppetlabs/server/bin/puppetserver", "foreground"]

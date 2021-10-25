# syntax=docker/dockerfile:1
FROM golang:1.17-alpine
ENV PUPPET_URL=127.0.0.1:8140
RUN apt-get update
RUN apt-get install puppet-agent
RUN puppet config set server $PUPPET_URL
RUN /opt/puppetlabs/bin/puppet resource service puppet ensure=running enable=true

# syntax=docker/dockerfile:1
FROM puppet/puppetserver

COPY manifests/ .

RUN puppet module install puppetlabs/vcsrepo
RUN puppet module generate git
RUN puppet agent --test --noop

EXPOSE 8140

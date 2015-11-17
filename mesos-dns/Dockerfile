FROM ubuntu:14.04
MAINTAINER jksun
ENV REFRESHED_AT 2014-11-25
RUN apt-get -qfy install curl

RUN curl -Ls https://github.com/mesosphere/mesos-dns/releases/download/v0.4.0/mesos-dns-v0.4.0-linux-amd64.gz -o mesos-dns.gz; \
	gunzip mesos-dns.gz; \
	rm -rf mesos-dns.gz;
RUN chmod +x mesos-dns
EXPOSE 53
EXPOSE 8123
ADD config.json config.json
ENTRYPOINT ["./mesos-dns"]

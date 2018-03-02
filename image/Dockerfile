FROM debian:stretch
MAINTAINER Phusion <info@phusion.nl>
Maintainer Julian Goestl <info@jgoestl.de>

COPY . /bd_build

RUN /bd_build/prepare.sh && \
	/bd_build/system_services.sh && \
	/bd_build/utilities.sh && \
	/bd_build/cleanup.sh

ENV DEBIAN_FRONTEND="teletype" \
    LANG="de_DE.UTF-8" \
    LANGUAGE="de_DE:de" \
    LC_ALL="de_DE.UTF-8"

CMD ["/sbin/my_init"]

FROM debian:latest
MAINTAINER Wanderley Santos "wysantos@gmail.com"

ENV DEBIAN_FRONTEND noninteractive

RUN apt update \
&& apt -y install \
apache2 \
php5 \
php5-mysql \
php5-ldap \
php5-xmlrpc \
php5-imap \
curl \
php5-curl \
php5-gd \
wget \
&& apt-get clean \
&& rm -rf /var/lib/apt/lists/*
RUN /usr/sbin/a2ensite default-ssl
RUN /usr/sbin/a2enmod ssl

ADD glpi-start.sh /opt/
RUN chmod +x /opt/glpi-start.sh
ENTRYPOINT ["/opt/glpi-start.sh"]

EXPOSE 80
EXPOSE 443

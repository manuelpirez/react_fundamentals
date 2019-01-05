FROM phpdockerio/php72-fpm:latest
WORKDIR "/application"

# Fix debconf warnings upon build
ARG DEBIAN_FRONTEND=noninteractive

# Install selected extensions and other stuff
RUN apt-get update \
    && apt-get -y --no-install-recommends install  php7.2-mysql php-xdebug php7.2-intl php7.2-ldap php-msgpack php7.2-odbc php7.2-phpdbg php7.2-pspell php-raphf php7.2-recode php7.2-soap php-ssh2 php7.2-sybase php-tideways php7.2-tidy php7.2-xmlrpc php7.2-xsl php-yaml php-zmq \
    && apt-get clean; rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* /usr/share/doc/*

# Install git
RUN apt-get update \
    && apt-get -y install git \
    && apt-get clean; rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* /usr/share/doc/*

#RUN apt-get update \
#    && apt install curl

##install node
#RUN curl -sL https://deb.nodesource.com/setup_10.x |  bash -
#RUN apt install nodejs && apt install nano
#
##install yarn
#RUN curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg |  apt-key add -
#    && echo "deb https://dl.yarnpkg.com/debian/ stable main" |  tee /etc/apt/sources.list.d/yarn.list
#    && sudo apt-get update && sudo apt-get install yarn





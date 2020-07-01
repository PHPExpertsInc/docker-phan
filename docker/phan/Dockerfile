# phpexperts/php:7
FROM phpexperts/php:7

ARG PHP_VERSION=7.4

# Fix add-apt-repository is broken with non-UTF-8 locales, see https://github.com/oerdnj/deb.sury.org/issues/56
ENV LC_ALL C.UTF-8
ENV DEBIAN_FRONTEND noninteractive

ADD https://getcomposer.org/composer.phar /usr/local/bin/composer

RUN apt-get update && \

    # Configure ondrej PPA
    apt-get install -y software-properties-common && \
    add-apt-repository ppa:ondrej/php && \
    apt-get update && \
    apt-get upgrade -y && \

    # Install php-ast
    apt-get install -y --no-install-recommends \
        php-ast && \

    # Cleanup
    apt-get autoremove -y && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/* && \
    rm -rf /var/cache/apt/* && \

    chmod +x /usr/local/bin/composer && \
    /usr/local/bin/composer global require 'phan/phan'

VOLUME ["/workdir"]
WORKDIR /workdir

ENTRYPOINT ["/root/.composer/vendor/bin/phan"]

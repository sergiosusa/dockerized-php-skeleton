FROM bitnami/php-fpm:7.4

RUN true \
 && apt-get -qq update \
 && apt-get -qy install --no-install-recommends \
        rsync \
        wget \
 && rm -rf /var/lib/apt/lists/* \
;

# Modify www-data user to match system user
ARG GROUP_ID=1000
ARG USER_ID=1000
RUN true \
 && groupmod www-data --gid "${GROUP_ID}" \
 && usermod www-data --uid "${USER_ID}" --gid www-data -d /var/www -s /bin/bash \
 && mkdir -p /var/www \
 && chown -R www-data:www-data /var/www

COPY www.conf "/opt/bitnami/php/etc/php-fpm.d/www.conf"

EXPOSE 9000

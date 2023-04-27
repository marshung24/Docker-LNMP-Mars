# 直接用 official image，可以省下很多工
FROM phpswoole/swoole:php8.1-alpine

COPY php.ini $PHP_INI_DIR/conf.d/

# 安裝 php extensions 的神器，請務必一試！
# https://github.com/mlocati/docker-php-extension-installer
COPY --from=mlocati/php-extension-installer /usr/bin/install-php-extensions /usr/bin/

RUN install-php-extensions redis mysqli xdebug
FROM appsvc/php:5.6.21-apache-0
MAINTAINER Nazim Lala <naziml@microsoft.com>

RUN yes | pecl install xdebug \
    && echo "zend_extension=$(find /usr/local/lib/php/extensions/ -name xdebug.so)" > /usr/local/etc/php/conf.d/xdebug.ini \
    && echo "xdebug.remote_enable=on" >> /usr/local/etc/php/conf.d/xdebug.ini \
    && echo "xdebug.remote_autostart=off" >> /usr/local/etc/php/conf.d/xdebug.ini \
    && echo "xdebug.profiler_output_dir=/home/LogFiles" >> /usr/local/etc/php/conf.d/xdebug.ini \

CMD ["/bin/init_container.sh"]

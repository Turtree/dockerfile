FROM quay.io/centos/centos:10

VOLUME /var/www/html /var/log/httpd
RUN yum -y install httpd mod_wsgi && yum clean all
COPY vhost.conf /etc/httpd/conf.d
COPY myapp.wsgi /var/www/html/myapp.wsgi

EXPOSE 80/tcp

# /usr/sbin/httpd -D FOREGROUND
ENTRYPOINT ["/usr/sbin/httpd", "-D", "FOREGROUND"]
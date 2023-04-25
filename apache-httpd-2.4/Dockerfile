FROM httpd:2.4.53

MAINTAINER nhattien.lam.545@gmail.com

COPY package /usr/local/apache2/htdocs
COPY conf/httpd.conf /usr/local/apache2/conf/httpd.conf
COPY conf/httpd-vhosts.conf /usr/local/apache2/conf/extra/httpd-vhosts.conf
COPY conf/httpd-ssl.conf /usr/local/apache2/conf/extra/httpd-ssl.conf
COPY --from=0 certificate/server.crt /usr/local/apache2/conf/server.crt
COPY --from=0 certificate/server.key /usr/local/apache2/conf/server.key
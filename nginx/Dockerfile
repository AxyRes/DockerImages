FROM nginx:latest
EXPOSE 80

MAINTAINER nhattien.lam.545@gmail.com

COPY conf/proxy.conf /etc/nginx/conf.d/
COPY package /usr/share/nginx/html

CMD ["nginx", "-g", "daemon off;"]
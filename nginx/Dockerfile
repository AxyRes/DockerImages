FROM nginx:latest

MAINTAINER nhattien.lam.545@gmail.com

COPY conf/default.conf /etc/nginx/conf.d/default.conf
COPY certificate /usr/local/ssl/certificate
COPY package /usr/share/nginx/html


CMD ["nginx", "-g", "daemon off;"]
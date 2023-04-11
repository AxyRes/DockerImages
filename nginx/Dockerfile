FROM nginx:latest
EXPOSE 80

MAINTAINER nhattien.lam.545@gmail.com

COPY conf/default.conf /etc/nginx/conf.d/default.conf
COPY package /usr/share/nginx/html

CMD ["nginx", "-g", "daemon off;"]
FROM nginx:latest

MAINTAINER nhattien.lam.545@gmail.com

COPY config/default.conf /etc/nginx/conf.d/default.conf
COPY certificate /usr/local/ssl/certificate


CMD ["nginx", "-g", "daemon off;"]
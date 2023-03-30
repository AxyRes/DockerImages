FROM tomcat:9.0.72-jdk17

MAINTAINER nhattien.lam.545@gmail.com

RUN apt update -y
RUN ln -snf /usr/share/zoneinfo/Asia/Ho_Chi_Minh /etc/localtime && echo Asia/Ho_Chi_Minh > /etc/timezone

WORKDIR /usr/local/tomcat/bin

CMD ["catalina.sh", "run"]
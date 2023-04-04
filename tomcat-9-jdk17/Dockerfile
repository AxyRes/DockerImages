FROM tomcat:9.0.72-jdk17

MAINTAINER nhattien.lam.545@gmail.com

RUN apt update -y
RUN ln -snf /usr/share/zoneinfo/Asia/Ho_Chi_Minh /etc/localtime && echo Asia/Ho_Chi_Minh > /etc/timezone

COPY source_file /usr/local/tomcat/webapps/source_file

WORKDIR /usr/local/tomcat/bin

CMD ["catalina.sh", "run"]
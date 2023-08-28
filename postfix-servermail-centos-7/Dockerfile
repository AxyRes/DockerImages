# Use an official CentOS base image
FROM centos:7

# Install Postfix
RUN yum install -y postfix curl zip unzip

# Copy your configuration files to the container
COPY conf/main.cf /etc/postfix/
COPY conf/master.cf /etc/postfix/
COPY etc/aliases /etc/
COPY sbin/sendmail.postfix /sbin/
COPY bin/mailq.postfix /bin/
COPY bin/newaliases.postfix /bin/

# Start Postfix on container startup
CMD ["postfix", "start-fg"]
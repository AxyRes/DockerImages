FROM centos:7

MAINTAINER nhattien.lam.545@gmail.com

RUN yum update -y && \
    yum install -y curl git zip unzip && \
    curl -fsSL https://get.docker.com -o get-docker.sh && \
    sh get-docker.sh && \
    rm get-docker.sh && \
    curl -L "https://github.com/docker/compose/releases/download/1.29.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose && \
    chmod +x /usr/local/bin/docker-compose

RUN curl -fsSL -o dotnet.tar.gz https://dotnetcli.azureedge.net/dotnet/Sdk/6.0.408/dotnet-sdk-6.0.408-linux-x64.tar.gz && \
    mkdir -p /usr/share/dotnet && \
    tar -zxf dotnet.tar.gz -C /usr/share/dotnet && \
    rm dotnet.tar.gz && \
    ln -s /usr/share/dotnet/dotnet /usr/bin/dotnet


CMD ["bash"]
FROM mcr.microsoft.com/mssql/server:2019-latest

MAINTAINER nhattien.lam.545@gmail.com

USER root

RUN apt-get update \
    && apt-get install -y zip unzip \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*

COPY $data /var/lib/mssql/$data
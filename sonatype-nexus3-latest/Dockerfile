FROM sonatype/nexus3

USER root

# Copy SSL certificate and key to Nexus SSL directory
COPY cert/nexus.crt /nexus-data/ssl/nexus.crt
COPY cert/nexus.key /nexus-data/ssl/nexus.key

# Set the Nexus context path and configure SSL
RUN echo "nexus-args=${karaf.etc}/jetty.xml,${karaf.etc}/jetty-http.xml,${karaf.etc}/jetty-requestlog.xml" >> /nexus-data/etc/nexus.properties && \
    echo "application-port-ssl=8082" >> /nexus-data/etc/nexus.properties && \
    echo "ssl.etc=${karaf.etc}/ssl" >> /nexus-data/etc/nexus.properties

# Set the permissions for SSL files
RUN chown -R nexus:nexus /nexus-data/ssl && \
    chmod 600 /nexus-data/ssl/nexus.key

USER nexus
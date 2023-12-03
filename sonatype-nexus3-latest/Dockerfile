FROM sonatype/nexus3

USER root

# Copy SSL certificate and key to Nexus SSL directory
COPY cert/nexus.crt /opt/sonatype/nexus/etc/ssl/nexus.crt
COPY cert/nexus.key /opt/sonatype/nexus/etc/ssl/nexus.key

# Set the Nexus context path and configure SSL
COPY config/nexus.properties /opt/sonatype/nexus/etc/nexus.properties

# Set the permissions for SSL files
RUN chown -R nexus:nexus /opt/sonatype/nexus/etc/ssl && \
    chmod 600 /opt/sonatype/nexus/etc/ssl/nexus.key

USER nexus
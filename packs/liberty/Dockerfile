#use open liberty runtime
FROM openliberty/open-liberty:javaee7
ENV PORT 9080
EXPOSE 9080
# Symlink servers directory for easier mounts.
RUN ln -s /opt/ol/wlp/usr/servers /servers


COPY target/*.war  target/*.jar /servers/defaultServer/dropins/

ENTRYPOINT ["/opt/ol/wlp/bin/server", "run"]
CMD ["defaultServer"]

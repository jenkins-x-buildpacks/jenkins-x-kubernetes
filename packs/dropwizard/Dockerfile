FROM openjdk:8-jdk-slim
EXPOSE 8080
EXPOSE 8081

# Copy the YAML configuration file to /opt/conf
COPY src/main/resources/application.yml /opt/conf/application.yml
ENV CONFIG_LOCATION /opt/conf/application.yml

# Copy the fat jar file to /opt. This assumes that there are up to four jar files:
#   original-app-1.0.0.jar
#   app-1.0.0.jar
#   app-1.0.0-sources.jar
#   app-1.0.0-javadoc.jar
#
COPY target/[^original]*[^javadoc][^sources].jar /opt/app.jar

WORKDIR /opt

# Start the Dropwizard application
CMD ["sh", "-c", "java -jar /opt/app.jar server ${CONFIG_LOCATION}"]

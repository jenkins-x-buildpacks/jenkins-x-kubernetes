FROM openjdk:8-jre-alpine
RUN mkdir -p /opt/app
WORKDIR /opt/app
COPY target/scala-*/*.jar /opt/app/app.jar
# we could do with a better way to know the name - or to always create an app.jar or something
WORKDIR /opt/app
CMD ["java", "-jar", "app.jar"]

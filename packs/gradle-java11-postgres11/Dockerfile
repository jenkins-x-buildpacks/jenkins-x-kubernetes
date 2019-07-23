FROM openjdk:11-jdk-slim
ENV PORT 8080
ENV SPRING_PROFILES_ACTIVE default
EXPOSE 8080
COPY build/libs/*.jar /opt/app.jar
WORKDIR /opt

CMD ["java", "-Dfile.encoding=UTF-8", "-Djava.security.egd=file:/dev/./urandom", "-Dspring.profiles.active=${SPRING_PROFILES_ACTIVE}", "-jar", "app.jar"]
FROM jenkins/jenkins:2.150.2
USER root
ENV CWP_VERSION 1.0-SNAPSHOT
ADD tmp/output/target/jenkins-x-serverless-${CWP_VERSION}.war /usr/share/jenkins/jenkins.war
RUN mkdir /app && unzip /usr/share/jenkins/jenkins.war -d /app/jenkins
COPY tmp/output/jenkinsfileRunner /app
RUN chmod +x /app/bin/jenkinsfile-runner && mkdir -p /usr/share/jenkins/ref/plugins
COPY tmp/output/plugins /usr/share/jenkins/ref/plugins

ENTRYPOINT ["/app/bin/jenkinsfile-runner", \
            "-w", "/app/jenkins",\
            "-p", "/usr/share/jenkins/ref/plugins",\
            "-f", "/workspace/Jenkinsfile"]

#FROM hashicorp/terraform:light
FROM jenkinsxio/builder-base:latest

# Install your tools and libraries
RUN yum -y install wget unzip && \
 wget https://releases.hashicorp.com/terraform/0.11.14/terraform_0.11.14_linux_amd64.zip && \
 unzip ./terraform_0.11.14_linux_amd64.zip -d /usr/local/bin/ 


#RUN mkdir -p /usr/src/app
#WORKDIR /usr/src/app
#COPY . /usr/src/app

ENTRYPOINT ["terraform", "-v"]
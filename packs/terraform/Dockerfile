FROM hashicorp/terraform:light


RUN mkdir -p /usr/src/app
WORKDIR /usr/src/app
COPY . /usr/src/app

ENTRYPOINT ["terraform"]
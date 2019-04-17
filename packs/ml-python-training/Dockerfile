FROM python:onbuild
RUN curl -f -L https://github.com/git-lfs/git-lfs/releases/download/v2.7.1/git-lfs-linux-amd64-v2.7.1.tar.gz | tar xzv \
./install.sh
RUN curl -f -L https://github.com/github/hub/releases/download/v2.11.2/hub-linux-amd64-2.11.2.tgz | tar xzv \
mv hub-linux-amd64-2.11.2/bin/hub /usr/bin
ENV JX_VERSION 2.0.4
RUN curl -f -L https://github.com/jenkins-x/jx/releases/download/v${JX_VERSION}/jx-linux-amd64.tar.gz | tar xzv && \
mv jx /usr/bin/
COPY requirements.txt .
ENV PORT 8080
EXPOSE 8080
ENTRYPOINT ["python"]
CMD ["app.py"]

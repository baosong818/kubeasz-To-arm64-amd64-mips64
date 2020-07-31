FROM debian:stable

ARG TARGETPLATFORM

COPY sources.list /etc/apt/sources.list

RUN apt-get update && \
    apt-get upgrade -y && \
    apt-get install -y procps ssh vim python2.7 ansible wget sshpass && \
    wget https://storage.googleapis.com/kubernetes-release/release/v1.15.12/bin/linux/amd64/kubectl -O /usr/bin/kubectl && \
    chmod +x /usr/bin/kubectl && \
    ln -s /usr/bin/python2.7 /usr/bin/python

COPY ansible /etc/ansible

WORKDIR /etc/ansible

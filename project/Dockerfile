# Pull base image.
FROM ubuntu

LABEL maintainer="Kevin <Kevin.kevin@xxxxxxxxxx.xxx>"
LABEL version="0.1"
LABEL description="This is custom Docker Image for \
ansible. I use this docker image in a project gitlab CI."

ENV DEBIAN_FRONTEND=noninteractive

# Install updates to base image
RUN apt-get update && \
    apt-get install -y gcc python2-dev libkrb5-dev && \
    apt-get install python3-pip -y && \
    pip3 install --upgrade pip && \
    pip3 install --upgrade virtualenv && \
    pip3 install pywinrm && \
    pip3 install kerberos && \
    apt install krb5-user -y && \
    pip3 install ansible && \
    apt install openssh-server openssh-client -y && \
    apt install sshpass -y

RUN mkdir /etc/ansible/

COPY ansible.cfg /etc/ansible/
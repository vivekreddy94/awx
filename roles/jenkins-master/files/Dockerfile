FROM jenkins/jenkins:lts
USER root
RUN apt-get update && \
    apt-get install -y sssd sudo && \
    apt-get install -y supervisor && \
    apt-get -y clean autoremove && \
    rm -rf /var/lib/apt/lists/*
COPY plugins.txt /usr/share/jenkins/ref/plugins.txt
RUN /usr/local/bin/install-plugins.sh < /usr/share/jenkins/ref/plugins.txt
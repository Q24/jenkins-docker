FROM jenkins/jenkins:2.249.2-lts-alpine

USER root

RUN echo http://dl-cdn.alpinelinux.org/alpine/edge/community >> /etc/apk/repositories && \
    apk -U add docker && \
    apk -U add py-pip && \
    apk -U add python3-dev libffi-dev openssl-dev gcc libc-dev make && \
    pip install docker-compose

RUN rm -rf /var/lib/apt/lists/* \
    /var/cache/apk/* \
    /usr/share/man \
    /tmp/*

RUN /usr/local/bin/install-plugins.sh pipeline-multibranch-defaults git workflow-aggregator blueocean greenballs ssh-steps email-ext mattermost filesystem_scm ws-cleanup basic-branch-build-strategies gitlab-plugin

VOLUME /var/run/docker.sock
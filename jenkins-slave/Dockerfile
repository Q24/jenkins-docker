FROM jenkins/agent:alpine

USER root

ENV JENKINS_URL = 
ENV JENKINS_TUNNEL = 
ENV JENKINS_SECRET = 
ENV JENKINS_AGENT_NAME = 
ENV JENKINS_AGENT_WORKDIR =
ENV JENKINS_WEB_SOCKET = 


RUN echo "http://dl-cdn.alpinelinux.org/alpine/edge/community" >> /etc/apk/repositories && \
    apk -U add --no-cache docker 

VOLUME /var/run/docker.sock

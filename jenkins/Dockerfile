FROM jenkins/jenkins:lts
LABEL maintainer=”darraghm.mccarthy@gmail.com”

USER root
RUN mkdir /var/log/jenkins
RUN mkdir /var/cache/jenkins
RUN chown -R jenkins:jenkins /var/log/jenkins
RUN chown -R jenkins:jenkins /var/cache/jenkins
USER jenkins

ENV JAVA_OPTS="-Xmx8192m"
ENV JENKINS_OPTS="--handlerCountMax=300 --httpPort=8082 --logfile=/var/log/jenkins/jenkins.log --webroot=/var/cache/jenkins/war"


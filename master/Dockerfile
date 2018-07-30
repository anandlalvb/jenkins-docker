FROM jenkins/jenkins:lts
# COPY plugins.txt /usr/share/jenkins/plugins.txt
# RUN /usr/local/bin/plugins.sh /usr/share/jenkins/plugins.txt
COPY install_plugins.txt /usr/share/jenkins/ref/install_plugins.txt
RUN /usr/local/bin/install-plugins.sh < /usr/share/jenkins/ref/install_plugins.txt
LABEL maintainer="anandl@rapidvaluesolutions.com"
COPY executors.groovy /usr/share/jenkins/ref/init.groovy.d/executors.groovy
COPY log.properties /usr/share/jenkins/ref/log.properties
COPY /jobs /usr/share/jenkins/ref/jobs
ENV JAVA_OPTS="-Xmx1024m"
ENV JENKINS_OPTS=" --handlerCountMax=300"

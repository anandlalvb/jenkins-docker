FROM jenkins/jenkins:lts
COPY plugins.txt /usr/share/jenkins/plugins.txt
RUN /usr/local/bin/plugins.sh /usr/share/jenkins/plugins.txt
LABEL maintainer="anandl@rapidvaluesolutions.com"
COPY executors.groovy /usr/share/jenkins/ref/init.groovy.d/executors.groovy
ENV JAVA_OPTS="-Xmx1024m"
ENV JENKINS_OPTS=" --handlerCountMax=300"

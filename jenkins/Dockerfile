FROM jenkins/jenkins:lts
EXPOSE 8080
EXPOSE 50000
COPY ../jdk-11.0.9.1+1 /opt/jdk-11
COPY ../apache-maven-3.6.3 /opt/maven
ENV JAVA_HOME=/opt/jdk-11
ENV PATH=/opt/maven/bin:/opt/jdk-11/bin:$PATH
CMD /usr/local/bin/jenkins.sh
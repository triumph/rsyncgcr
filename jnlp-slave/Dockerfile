FROM jicki/jenkins-jnlp

MAINTAINER triumph2008 <triumph2008@gmail.com>

ENV MAVEN_VERSION 3.3.9

RUN wget -q http://archive.apache.org/dist/maven/maven-3/$MAVEN_VERSION/binaries/apache-maven-$MAVEN_VERSION-bin.tar.gz -O - | tar xzf - && \
    mv /tmp/apache-maven-$MAVEN_VERSION /usr/lib/maven && \
    ln -s /usr/lib/maven/bin/mvn /usr/bin/mvn && \
    rm -rf /tmp/apache-maven* 
    
USER jenkins
ENTRYPOINT ["jenkins-slave"]

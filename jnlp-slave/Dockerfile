FROM jicki/jenkins-jnlp

MAINTAINER triumph2008 <triumph2008@gmail.com>

ENV MAVEN_VERSION 3.3.9

RUN cd /tmp && wget -q http://archive.apache.org/dist/maven/maven-3/3.3.9/binaries/apache-maven-3.3.9-bin.tar.gz -O /tmp/maven.tar.gz &&  tar xzf /tmp/maven.tar.gz -C /tmp && \
    mv /tmp/apache-maven-3.3.9 /usr/lib/maven && \
    ln -s /usr/lib/maven/bin/mvn /usr/bin/mvn && \
    rm -rf /tmp/apache-maven* && \
    rm -rf /tmp/maven.tar.gz 
    
USER jenkins
ENTRYPOINT ["jenkins-slave"]

FROM ubuntu:16.04
RUN apt-get update
RUN apt-get -y install software-properties-common
RUN add-apt-repository ppa:webupd8team/java
RUN apt-get -y update
RUN echo "oracle-java7-installer shared/accepted-oracle-license-v1-1 boolean true" | debconf-set-selections
RUN apt-get -y install oracle-java8-installer
ENV JAVA_HOME="/usr/lib/jvm/java-8-oracle"
COPY ./TodoDemo-0.0.1-SNAPSHOT.war /TodoDemo-0.0.1-SNAPSHOT.war
CMD ["java","-jar","/TodoDemo-0.0.1-SNAPSHOT.war"]

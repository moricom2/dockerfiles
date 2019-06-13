FROM moricom/ubuntu-ko:latest
RUN apt-get update && apt-get install -y \
    wget \
    tar \
    vim \
    git \
    openjdk-8-jdk
RUN wget http://mirror.apache-kr.org/maven/maven-3/3.6.1/binaries/apache-maven-3.6.1-bin.tar.gz
RUN tar xzvf apache-maven-3.6.1-bin.tar.gz -C /usr/share/
RUN update-alternatives --install /usr/bin/mvn mvn /usr/share/apache-maven-3.6.1/bin/mvn 9999
WORKDIR /workspace
RUN git clone https://github.com/moricom2/springboot-api-service.git
WORKDIR ./springboot-api-service
RUN rm -rf .git && mvn install
WORKDIR /workspace
RUN rm -rf *

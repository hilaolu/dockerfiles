FROM debian:bullseye-slim 

ENV PATH="/usr/local/jdk11/bin:${PATH}"

# Install sbt
RUN \
  apt update && \
  apt install curl -y && \
  mkdir -p /usr/local/ && \
  cd /usr/local/ && \
  curl -L -o jdk.tar.gz https://github.com/alibaba/dragonwell11/releases/download/dragonwell-11.0.12.8_jdk-11.0.12-ga/Alibaba_Dragonwell_11.0.12.8_x64_linux.tar.gz && \
  tar xvf jdk.tar.gz && \
  mv jdk-11.0.12.8* jdk11 && \
  java --version
  
  


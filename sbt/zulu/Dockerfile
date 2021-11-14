FROM azul/zulu-openjdk-debian:11

ARG SBT_VERSION=1.4.9

# Install sbt
RUN \
  apt update && \
  apt install curl -y && \
  mkdir /working/ && \
  cd /working/ && \
  curl -L -o sbt-$SBT_VERSION.deb https://repo.scala-sbt.org/scalasbt/debian/sbt-$SBT_VERSION.deb && \
  dpkg -i sbt-$SBT_VERSION.deb && \
  rm sbt-$SBT_VERSION.deb && \
  apt-get update && \
  apt-get install sbt -y && \
  cd && \
  rm -r /working/ && \
  sbt sbtVersion

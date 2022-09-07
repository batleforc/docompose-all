FROM maven:3.8.6-eclipse-temurin-11

RUN apt-get update && apt-get install -y \
  curl

RUN curl -fkL https://github.com/coursier/launchers/raw/master/cs-x86_64-pc-linux.gz | gzip -d > cs && chmod +x cs && ./cs setup -y

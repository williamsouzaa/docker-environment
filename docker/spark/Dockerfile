FROM ubuntu:latest

RUN apt-get update --yes

RUN apt-get install --yes curl \ 
  wget \
  tar \
  bash \
  software-properties-common \
  python-is-python3 \
  default-jdk \
  scala

RUN mkdir /home/Projects

ENV JAVA_HOME="/usr/lib/jvm/java-11-openjdk-amd64"

RUN wget https://dlcdn.apache.org/spark/spark-3.3.2/spark-3.3.2-bin-hadoop3.tgz

RUN tar xvf spark-*

RUN mv spark-3.3.2-bin-hadoop3 /opt/spark

ENV SPARK_HOME="/opt/spark"
ENV PATH="$PATH:$SPARK_HOME/bin:$SPARK_HOME/sbin"
ENV PYSPARK_PYTHON="/usr/bin/python3"

RUN rm -rf spark-*

WORKDIR /home/Projects 

ENTRYPOINT ["bash"]
ENTRYPOINT ["tail", "-f", "/dev/null"]


FROM openjdk:8-alpine

RUN apk --update add wget tar bash

# RUN wget http://apache.mirror.digitalpacific.com.au/spark/spark-2.4.1/spark-2.4.1-bin-hadoop2.7.tgz
# RUN wget https://downloads.apache.org/spark/spark-3.2.0/spark-3.2.0-bin-hadoop3.2.tgz 
RUN wget https://downloads.apache.org/spark/spark-3.2.0/spark-3.2.0-bin-hadoop3.2-scala2.13.tgz

RUN tar -xzf spark-3.2.0-bin-hadoop3.2-scala2.13.tgz && \
    mv spark-3.2.0-bin-hadoop3.2-scala2.13 /spark && \
    rm spark-3.2.0-bin-hadoop3.2-scala2.13.tgz

ENV SPARK_HOME=/spark
ENV PATH=$PATH:$SPARK_HOME/bin:$SPARK_HOME/sbin

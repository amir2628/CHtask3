FROM ubuntu:22.04

WORKDIR /task

ADD . /task

RUN set -xe \
    && apt-get update -y \
    && apt-get install -y python3-pip \
    && apt-get install -y time

RUN pip3 install joblib
RUN pip3 install scalene
RUN pip3 install numpy
RUN pip3 install scipy
RUN pip3 install scikit-learn 
RUN pip3 install pandas
RUN pip3 install psutil


COPY train.csv ./train.csv
COPY test.csv ./test.csv

COPY train.py ./train.py
COPY inference.py ./inference.py

RUN python3 train.py

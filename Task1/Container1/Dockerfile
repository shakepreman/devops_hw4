FROM ubuntu:14.04
MAINTAINER Abhishek Preman, apreman@ncsu.edu

RUN apt-get -y update
RUN apt-get -y install socat
RUN echo "Creating a test file" > test.txt
CMD socat TCP4-LISTEN:9001 SYSTEM:'cat test.txt'

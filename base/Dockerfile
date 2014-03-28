FROM ubuntu:latest

ENV DEBIAN_FRONTEND noninteractive
RUN apt-get update
RUN apt-get install -y \
    build-essential python-pip libcrypto++-dev python-dev libssl-dev \
	libffi-dev
RUN pip install Twisted
RUN pip install Nevow
RUN pip install allmydata-tahoe
RUN mkdir /tahoe
RUN chown daemon:daemon /tahoe
USER daemon

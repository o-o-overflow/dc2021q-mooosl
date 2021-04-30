FROM ubuntu:20.04

RUN apt-get -qq update && apt-get install -qq --no-install-recommends gcc python3-pip

RUN pip3 install pwntools

COPY exploit.py /


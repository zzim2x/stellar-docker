FROM ubuntu:14.04

RUN apt update && apt install -y \
  software-properties-common python-software-properties
RUN add-apt-repository ppa:ubuntu-toolchain-r/test
RUN apt update && apt install -y \
  git build-essential pkg-config autoconf automake libtool bison flex \
  libpq-dev clang++-3.5 gcc-4.9 g++-4.9 cpp-4.9

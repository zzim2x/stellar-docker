FROM zzim2x/ubuntu-dev:14.04

ENV STELLAR_VERSION v9.2.0

RUN apt install -y pandoc

RUN mkdir -p /opt/src

RUN cd /opt/src && git clone https://github.com/stellar/stellar-core -b $STELLAR_VERSION
RUN cd /opt/src/stellar-core && git submodule init && git submodule update

WORKDIR /opt/src/stellar-core

RUN ./autogen.sh
RUN CXX=g++-4.9 ./configure
RUN make
RUN make install


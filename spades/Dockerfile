FROM ubuntu:18.04

ARG SPAdesVer=3.15.5
# install dependencies; cleanup apt garbage
# python v2.7.12 is installed here
RUN apt-get update && apt-get install -y python \
 wget zip && \
 apt-get autoclean && rm -rf /var/lib/apt/lists/*

# install awscli
RUN wget -P /usr/src/ https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip && \
    unzip -d /usr/src/ /usr/src/awscli-exe-linux-x86_64.zip && \
    rm /usr/src/awscli-exe-linux-x86_64.zip && \
    /usr/src/aws/install

# install SPAdes binary; make /data
RUN wget https://github.com/ablab/spades/releases/download/v${SPAdesVer}/SPAdes-${SPAdesVer}-Linux.tar.gz && \
  tar -xzf SPAdes-${SPAdesVer}-Linux.tar.gz && \
  rm -r SPAdes-${SPAdesVer}-Linux.tar.gz && \
  mkdir /data

COPY ./conf/ /conf/
COPY ./src/ /src/

ENV PATH="${PATH}:/SPAdes-${SPAdesVer}-Linux/bin"

WORKDIR /data

CMD ["/bin/bash", "-c"]

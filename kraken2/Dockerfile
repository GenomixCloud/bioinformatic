FROM ubuntu:22.04

ARG K2pVer="2.1.3"

# install dependencies
RUN apt-get update && \
    apt-get upgrade -y perl && \
    apt-get install -y \
    zlib1g-dev \
    make \
    wget \
    zip

RUN apt install python3 -y

RUN apt-get install -y \
    g++ \
    rsync \
    unzip \
    ncbi-blast+ && \
    rm -rf /var/lib/apt/lists/* && apt-get autoclean

# install awscli
RUN wget -P /usr/src/ https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip && \
    unzip -d /usr/src/ /usr/src/awscli-exe-linux-x86_64.zip && \
    rm /usr/src/awscli-exe-linux-x86_64.zip && \
    /usr/src/aws/install

# getting kraken2
RUN wget -P /usr/local/ https://github.com/DerrickWood/kraken2/archive/v${K2pVer}.tar.gz && \
    tar -xzf /usr/local/v${K2pVer}.tar.gz -C /usr/local/ && \
    rm -rf /usr/local/v${K2pVer}.tar.gz
RUN cd /usr/local/kraken2-${K2pVer} && \
 ./install_kraken2.sh .

COPY ./conf/* /conf/
COPY ./src/* /src/

# overriding locales. It's not recommended
# https://www.baeldung.com/linux/locale-environment-variables#3-lcall-environment-variable
ENV PATH="$PATH:/usr/local/kraken2-${K2pVer}" \
    LC_ALL=C

WORKDIR /data

CMD ["/bin/bash", "-c"]

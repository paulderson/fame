FROM ubuntu:focal

WORKDIR /opt

RUN apt-get update && \
  apt-get upgrade -y

RUN apt-get install -y \
  python3-dev \
  python3-pip

RUN apt-get install -y \
  git \
  screen \
  p7zip-full \
  libjpeg-dev \
  zlib1g-dev

RUN apt-get install -y \
  apt-transport-https \
  ca-certificates

RUN apt-get install -y \
  curl \
  gnupg2

RUN apt-get install -y \
  wget \
  nano

RUN DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata

RUN DEBIAN_FRONTEND=noninteractive apt-get install -y \
  software-properties-common

RUN apt install -y docker.io
RUN pip3 install virtualenv

ENTRYPOINT ["tail", "-f", "/dev/null"]
EXPOSE 4200

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

# RUN wget -qO - https://www.mongodb.org/static/pgp/server-4.4.asc | apt-key add -

# Ubuntu
# RUN echo "deb [ arch=amd64,arm64 ] https://repo.mongodb.org/apt/ubuntu focal/mongodb-org/4.4 multiverse" | tee /etc/apt/sources.list.d/mongodb-org-4.4.list

# RUN apt-get update && apt-get install -y \
#     mongodb-org

# RUN curl -fsSL https://download.docker.com/linux/ubuntu/gpg | apt-key add -
# RUN add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu focal stable"
# RUN apt-get update && apt-get install -y \
#     docker-ce \
#     docker-ce-cli \
#     containerd.io

RUN apt install -y docker.io

RUN pip3 install virtualenv
# RUN git clone https://github.com/paulderson/fame.git
# ENTRYPOINT ["/opt/fame/docker/donothing.sh"]
ENTRYPOINT ["tail", "-f", "/dev/null"]
EXPOSE 4200

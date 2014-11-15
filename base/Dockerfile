# Usage:
# > sudo docker run -ti -u ctemplin -v /home/ctemplin:/home/ctemplin devbase

FROM ubuntu:trusty
RUN apt-get update
RUN apt-get -y install ruby ruby-dev build-essential git
RUN apt-get install -y openssl
RUN apt-get install -y curl

# For debugging
RUN apt-get install -y gdb strace

# Set up my user
RUN useradd ctemplin -u 1000 -s /bin/bash --no-create-home

RUN gem install -n /usr/bin bundler
RUN gem install -n /usr/bin rake

WORKDIR /home/ctemplin/
ENV HOME /home/ctemplin

VOLUME ["/home"]
USER ctemplin
EXPOSE 8080
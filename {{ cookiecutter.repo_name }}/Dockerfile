FROM ubuntu:18.04

# Install python3
RUN apt-get update \
  && apt-get install -y python3-pip python3.6 \
  && cd /usr/local/bin \
  && ln -s /usr/bin/python3 python \
  && pip3 install --upgrade pip \
  && apt-get install -y zsh \
  && apt-get install -y wget \
  && apt-get install -y curl

RUN apt-get install -y git

RUN sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)" -y

# Install pipenv
RUN pip install pipenv

# Install nano
RUN apt-get install nano

# export variables to avoid issues with pipenv
RUN echo "export LC_ALL=C.UTF-8" >> ~/.zshrc
RUN echo "export LANG=C.UTF-8" >> ~/.zshrc
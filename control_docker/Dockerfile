FROM ubuntu:20.04

ARG DEBIAN_FRONTEND=noninteractive

RUN apt-get update
RUN apt-get install --yes \
      python3 python3-pip rpm git vim \
      openconnect

RUN pip3 install ansible

COPY . /pire-playbooks
RUN /pire-playbooks/init-roles

WORKDIR /pire-playbooks

CMD ["/bin/bash"]

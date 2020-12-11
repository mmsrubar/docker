FROM centos:8

RUN dnf update -y
RUN dnf install -y nmap
RUN dnf install -y telnet
RUN dnf install -y bind-utils
RUN dnf install -y openssh-clients
RUN dnf install -y wget
RUN dnf install -y curl

RUN echo "set -o vi" >> /root/.bashrc   # god-like mode
RUN echo "alias vim=\"/usr/bin/vi\"" >> /root/.bashrc
RUN echo "alias ll=\"ls -ls\"" >> /root/.bashrc

ENTRYPOINT ["/bin/bash"]

FROM centos:8

RUN dnf update -y
RUN dnf install -y dhcp-server

RUN dnf install -y man vim
WORKDIR /etc/dhcp

COPY dhcpd.conf /etc/dhcp/dhcpd.conf
CMD ["/usr/sbin/dhcpd", "-user", "dhcpd", "-group", "dhcpd", "-f", "-d"]

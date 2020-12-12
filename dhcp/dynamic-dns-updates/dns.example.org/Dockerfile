FROM centos:8

RUN dnf update -y
RUN dnf install bind -y
RUN dnf install bind-utils -y
RUN mkdir /etc/bind
RUN mkdir /var/log/bind

EXPOSE 53
WORKDIR /etc/bind

COPY named.conf /etc/bind/named.conf
COPY db.example.org /etc/bind/db.example.org
COPY db.192.168.100 /etc/bind/db.192.168.100

RUN chown named:named -R /etc/bind
RUN chown named:named -R /var/log/bind

CMD ["/usr/sbin/named", "-u", "named", "-g", "-c", "/etc/bind/named.conf"]

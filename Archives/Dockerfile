FROM ubuntu:latest as builder

COPY banner.sh /etc/banner
COPY entrypoint /etc/entrypoint
COPY ./challenges /root/challenges

RUN chmod +x /etc/entrypoint /etc/banner

COPY shell.sh /usr/local/bin/shell.sh
RUN chmod +x /usr/local/bin/shell.sh
RUN usermod --shell /usr/local/bin/shell.sh root

WORKDIR /root

ENTRYPOINT ["/etc/entrypoint"]

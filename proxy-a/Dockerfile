FROM ubuntu:latest
ENV DEBIAN_FRONTEND noninteractive
RUN apt-get update && apt-get install -y squid
ADD squid.conf /etc/squid/squid.conf
CMD ["/bin/bash"]

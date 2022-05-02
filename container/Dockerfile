FROM golang:1.18

RUN \
    useradd -m -s '/bin/bash' -p "$(openssl passwd -1 dev)" dev; \
    usermod -aG sudo dev; \
    echo "PATH=$PATH:/usr/local/go/bin" >> /home/dev/.profile
RUN \
    apt-get update -y; \
    apt-get install sudo -y; \
    apt-get install nano -y; \
    apt-get install iproute2 -y; \
    apt-get install iputils-ping -y; \
    apt-get install traceroute -y; \
    apt-get install tcpdump -y; \
    apt-get install dhcpdump -y; \
    apt-get install tree -y; \
    apt-get install python-is-python3 -y; \
    apt-get install openssh-server -y; \
    systemctl enable ssh

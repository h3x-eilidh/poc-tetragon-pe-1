FROM ubuntu:latest

RUN apt-get update -y && apt-get install sudo -y

RUN useradd -m -u 1000 userx

RUN echo "userx:userx" | chpasswd

RUN echo "userx ALL=(ALL:ALL) /usr/bin/find" >> /etc/sudoers

USER userx

CMD ["tail", "-f", "/dev/null"]

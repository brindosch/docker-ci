# Base image to compile Hyperion for Raspberry Pi (Raspbian Stretch) with Docker as cross compilation through qemu
# You can start this container also with bash access: sudo docker run -it hyperionorg/hyperion-ci:rpistretch /bin/bash

FROM resin/rpi-raspbian:stretch

ENV QEMU_EXECVE 1

COPY . /usr/bin

RUN [ "qemu-arm-static", "/bin/sh", "-c", "ln -s resin-xbuild /usr/bin/cross-build-start; ln -s resin-xbuild /usr/bin/cross-build-end; mv /bin/sh /bin/sh.real; ln -s /bin/sh.real /bin/sh" ]

RUN [ "cross-build-start" ]

# install hyperion compile deps
# additional zlib1g-dev and libraspberrypi-dev
RUN apt-get update && apt-get install -y git cmake python3-dev qtbase5-dev libqt5serialport5-dev build-essential libusb-1.0-0-dev libavahi-core-dev libavahi-compat-libdnssd-dev zlib1g-dev libraspberrypi-dev

RUN [ "cross-build-end" ]

# we use always qemu
ENTRYPOINT ["/usr/bin/qemu-arm-static"]
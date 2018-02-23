# Base image to compile Hyperion on a Raspberry Pi FOR Raspberry Pi (Raspbian Stretch)

FROM resin/rpi-raspbian:stretch

# install hyperion compile deps
# additional zlib1g-dev and libraspberrypi-dev
RUN apt-get update && apt-get install -y git cmake python3-dev qtbase5-dev libqt5serialport5-dev build-essential libusb-1.0-0-dev libavahi-core-dev libavahi-compat-libdnssd-dev zlib1g-dev libraspberrypi-dev


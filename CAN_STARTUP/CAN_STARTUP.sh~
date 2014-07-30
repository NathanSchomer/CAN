#!/bin/sh


#place overlay
cp /home/root/CAN/CAN_STARTUP/BB-DCAN1-00A0.dtbo /lib/firmware
echo BB-DCAN1 > /sys/devices/bone_capemgr.9/slots

#import modules
modprobe can
modprobe can-dev
modprobe can-raw

#setup and enable CAN bus
ip link set can0 up type can bitrate 1000000
ifconfig can0

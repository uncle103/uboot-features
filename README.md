# 1. Build Guide

## 1.1 Arm build for board vexpress_ca9x4

export ARCH=arm

export CROSS_COMPILE=arm-linux-gnueabi-

make  vexpress_ca9x4_defconfig | tee log

make -j4

## 1.2 Arm build for board ti814x

export ARCH=arm

export CROSS_COMPILE=arm-linux-gnueabi-

make  ti814x_evm_defconfig

make  "CFLAGS+= -g OPTFLAGS= -Os" -j4| tee log

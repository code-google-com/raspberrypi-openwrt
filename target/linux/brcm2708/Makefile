#
# Copyright (C) 2012 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#
include $(TOPDIR)/rules.mk

ARCH:=arm
BOARD:=brcm2708
BOARDNAME:=Broadcom BCM2708/BCM2835
FEATURES:=ext4 audio usb usbgadget display gpio fpu
MAINTAINER:=Nathan Huizinga <nathan[dot]huizinga[at]gmail.com>

LINUX_VERSION:=3.6.11
#LINUX_VERSION:=3.3.8

include $(INCLUDE_DIR)/target.mk
DEFAULT_PACKAGES += brcm2708-gpu-fw kmod-usb-hid kmod-sound-core kmod-sound-arm-bcm2835

define Target/Description
	Build firmware image for Broadcom BCM2708/BCM2835 SoC devices.
	Currently produces SD Card image for Raspberry Pi.
endef

CFLAGS:=-O2 -pipe -march=armv6 -mtune=arm1176jzf-s -mfpu=vfp -mfloat-abi=softfp -marm

KERNELNAME:="Image"

$(eval $(call BuildTarget))

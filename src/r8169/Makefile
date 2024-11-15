# SPDX-License-Identifier: GPL-2.0-only
#
# Makefile for the Realtek network device drivers.
#

obj-m := r8169.o
r8169-objs := r8169_main.o r8169_firmware.o r8169_phy_config.o

ifeq ($(CONFIG_R8169_LEDS), y)
	r8169-objs += r8169_leds.o
	EXTRA_CFLAGS += -DCONFIG_R8169_LEDS
endif

ifeq ($(CONFIG_ATP), y)
	r8169-objs += atp.o
	EXTRA_CFLAGS += -DCONFIG_ATP
endif

ifeq ($(CONFIG_8139CP), y)
	r8169-objs += 8139cp.o
	EXTRA_CFLAGS += -DCONFIG_8139CP
endif

ifeq ($(CONFIG_8139TOO), y)
	r8169-objs += 8139too.o
	EXTRA_CFLAGS += -DCONFIG_8139TOO
endif
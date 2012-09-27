#
# Makefile for the Linux Bluetooth subsystem.
#

ifdef CONFIG_CC_OPTIMIZE_ALOT
CFLAGS_l2cap_core.o += -O2
endif
ifdef CONFIG_CC_OPTIMIZE_FAST
CFLAGS_l2cap_core.o += -O2
endif

obj-$(CONFIG_BT)	+= bluetooth.o
obj-$(CONFIG_BT_RFCOMM)	+= rfcomm/
obj-$(CONFIG_BT_BNEP)	+= bnep/
obj-$(CONFIG_BT_CMTP)	+= cmtp/
obj-$(CONFIG_BT_HIDP)	+= hidp/
obj-$(CONFIG_BT_HID_BRCM)	+= hidbrcm/

bluetooth-y := af_bluetooth.o hci_core.o hci_conn.o hci_event.o mgmt.o hci_sock.o hci_sysfs.o lib.o smp.o
bluetooth-$(CONFIG_BT_L2CAP)	+= l2cap_core.o l2cap_sock.o amp.o
bluetooth-$(CONFIG_BT_SCO)	+= sco.o

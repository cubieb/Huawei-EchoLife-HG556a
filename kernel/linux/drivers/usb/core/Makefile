#
# Makefile for USB Core files and filesystem
#
EXTRA_CFLAGS += -I$(INC_BRCMDRIVER_PUB_PATH)/$(BRCM_BOARD)
usbcore-objs	:= usb.o hub.o hcd.o urb.o message.o \
			config.o file.o buffer.o sysfs.o

ifeq ($(CONFIG_PCI),y)
	usbcore-objs	+= hcd-pci.o
endif

ifeq ($(CONFIG_USB_DEVICEFS),y)
	usbcore-objs	+= devio.o inode.o devices.o
endif

obj-$(CONFIG_USB)	+= usbcore.o

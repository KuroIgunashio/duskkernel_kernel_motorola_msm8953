#
# Makefile for the Kinibi core driver
#

GUD_ROOT_FOLDER := drivers/gud/

# add our modules to kernel.
obj-$(CONFIG_TRUSTONIC_TEE) += mcDrvModule.o

mcDrvModule-y := \
	admin.o \
	client.o \
	clientlib.o \
	clock.o \
	fastcall.o \
	iwp.o \
	logging.o \
	main.o \
	mcp.o \
	mmu.o \
	nq.o \
	pm.o \
	scheduler.o \
	session.o \
	teeclientapi.o \
	user.o

# Release mode by default
# DHV
#ccflags-y += -DNDEBUG
ccflags-y += -DDEBUG
ccflags-y += -Wno-declaration-after-statement

ccflags-$(CONFIG_TRUSTONIC_TEE_DEBUG) += -DDEBUG

# MobiCore Driver includes
ccflags-y += -I$(GUD_ROOT_FOLDER)/MobiCoreDriver

obj-m += libshared.mod
obj-libshared-static := yes

obj-libshared-m := \
    sol-fbp-graph.o \
    sol-fbp-internal-log.o \
    sol-fbp-internal-scanner.o \
    sol-monitors.o \
    sol-util.o

ifeq (y,$(RESOLVER_CONFFILE))
obj-libshared-m += \
    sol-fbp-parser.o
endif

ifeq (y,$(PLATFORM_RIOTOS))
obj-libshared-m += \
    sol-network-riot.o
endif

ifeq (y,$(SOL_PLATFORM_LINUX))
obj-libshared-m += \
    sol-conffile.o \
    sol-file-reader.o \
    sol-network-linux.o
obj-libshared-m-extra-cflags += $(GLIB_CFLAGS)
obj-libshared-m-extra-ldflags += $(GLIB_LDFLAGS)
endif

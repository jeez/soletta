obj-$(IO) += io.mod

obj-io-$(IO) := \
    sol-gpio-common.o \
    sol-i2c-common.o \
    sol-pwm-common.o \

ifeq (y,$(PLATFORM_RIOTOS))
obj-io-$(IO) += \
    sol-gpio-riot.o \
    sol-i2c-riot.o \
    sol-pwm-riot.o \
    sol-spi-riot.o \
    sol-uart-riot.o
endif

ifeq (y,$(SOL_PLATFORM_LINUX))
obj-io-$(IO) += \
    sol-gpio-linux.o \
    sol-i2c-linux.o \
    sol-pwm-linux.o \
    sol-spi-linux.o \
    sol-uart-linux.o
endif

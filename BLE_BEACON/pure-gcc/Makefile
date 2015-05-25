SHELL=C:/Windows/System32/cmd.exe
# List all source files the application uses.
APPLICATION_SRCS = $(notdir $(wildcard ../*.c))
APPLICATION_SRCS += app_gpiote.c
APPLICATION_SRCS += app_button.c
APPLICATION_SRCS += app_timer.c
APPLICATION_SRCS += app_trace.c
APPLICATION_SRCS += ble_advdata.c
APPLICATION_SRCS += ble_conn_params.c
APPLICATION_SRCS += pstorage.c
APPLICATION_SRCS += device_manager_peripheral.c
APPLICATION_SRCS += ble_bas.c
APPLICATION_SRCS += ble_dis.c
APPLICATION_SRCS += ble_hrs.c
APPLICATION_SRCS += ble_srv_common.c
APPLICATION_SRCS += crc16.c
APPLICATION_SRCS += softdevice_handler.c
APPLICATION_SRCS += nrf_delay.c

PROJECT_NAME = $(shell basename "$(realpath ../)")

DEVICE = NRF51
BOARD = BOARD_PCA10001
#SEGGER_SERIAL = 518004431

USE_SOFTDEVICE = s110

#SDK_PATH = $(HOME)/Projects/nrf51-sdk-6.0.0/nrf51822/
#TEMPLATE_PATH = $(HOME)/Projects/nrf51-pure-gcc-setup/template/
SDK_PATH = ../../../nrf51822_sdk/
TOOLCHAIN_PATH = $(SDK_PATH)arm-gcc/bin/
TEMPLATE_PATH = $(SDK_PATH)nrf51-pure-gcc-setup/template/

#SOFTDEVICE = $(SDK_PATH)softdevice/s110_nrf51822_6.0.0_softdevice.hex
SOFTDEVICE = $(SDK_PATH)softdevice/s110_nrf51822_7.1.0_softdevice.hex
#CFLAGS = -Os
#CFLAGS += -ffunction-sections -fdata-sections -fno-strict-aliasing
#CFLAGS += -flto -fno-builtin
CFLAGS += -DDEBUG -ggdb -O0 # ligne a ajouter dans le makefile 
GDB_PORT_NUMBER = 2331

include $(TEMPLATE_PATH)Makefile

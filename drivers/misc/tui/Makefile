#
# Makefile for the stui Module
#

obj-$(CONFIG_SAMSUNG_TUI)	+= main.o
obj-$(CONFIG_SAMSUNG_TUI)	+= stui_core.o
obj-$(CONFIG_SAMSUNG_TUI)	+= stui_inf.o

ifeq ($(CONFIG_SOC_EXYNOS3250),y)
obj-$(CONFIG_SAMSUNG_TUI)	+= platforms/exynos3250/
endif
ifeq ($(CONFIG_SOC_EXYNOS7420),y)
obj-$(CONFIG_SAMSUNG_TUI)	+= platforms/exynos7420/
endif
ifeq ($(CONFIG_SOC_EXYNOS7885),y)
obj-$(CONFIG_SAMSUNG_TUI)	+= platforms/exynos7885/
endif
ifeq ($(CONFIG_SOC_EXYNOS8895),y)
obj-$(CONFIG_SAMSUNG_TUI)	+= platforms/exynos8895/
endif
ifeq ($(CONFIG_SOC_EXYNOS9610),y)
ccflags-$(CONFIG_SAMSUNG_TUI)	+= -DUSE_TEE_CLIENT_API
ccflags-$(CONFIG_SAMSUNG_TUI)	+= -Idrivers/misc/tzdev/include/tzdev
obj-$(CONFIG_SAMSUNG_TUI)	+= platforms/exynos9610/
endif
ifeq ($(CONFIG_SOC_EXYNOS9820),y)
ccflags-$(CONFIG_SAMSUNG_TUI)	+= -DUSE_TEE_CLIENT_API
ccflags-$(CONFIG_SAMSUNG_TUI)	+= -Idrivers/misc/tzdev/include/tzdev
obj-$(CONFIG_SAMSUNG_TUI)	+= platforms/exynos9820/
endif
ifeq ($(CONFIG_MACH_MT6757),y)
obj-$(CONFIG_SAMSUNG_TUI)	+= platforms/mt6757/
endif

ccflags-$(CONFIG_SAMSUNG_TUI_TEST)	+= -DSAMSUNG_TUI_TEST
obj-$(CONFIG_SAMSUNG_TUI_TEST)	+= test_driver/

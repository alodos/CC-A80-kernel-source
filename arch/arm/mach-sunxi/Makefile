ifneq ($(strip $(CONFIG_ARCH_SUN4I) $(CONFIG_ARCH_SUN5I)),)
obj-y += sun4i.o
endif

ifneq ($(strip $(CONFIG_ARCH_SUN6I) $(CONFIG_ARCH_SUN7I)),)
obj-y += sun6i.o
endif

ifneq ($(strip $(CONFIG_ARCH_SUN8I)),)
obj-y += sun8i.o
obj-$(CONFIG_SW_POWERNOW) += powernow.o
obj-$(CONFIG_PM) += pm/
endif

ifneq ($(strip $(CONFIG_ARCH_SUN8IW6)),)
obj-$(CONFIG_SMP)       += sun8i-platsmp.o
obj-$(CONFIG_SUN8I_CCI) += sun8i-cci.o
obj-$(CONFIG_MCPM)      += sun8i-setup.o sun8i-mcpm.o
endif

ifneq ($(strip $(CONFIG_ARCH_SUN9I)),)
obj-y                   += sun9i.o
obj-$(CONFIG_SW_POWERNOW) += powernow.o
obj-$(CONFIG_SW_POWERNOW) += powernow_cpu.o
obj-$(CONFIG_SMP)       += sun9i-platsmp.o
obj-$(CONFIG_SUN9I_CCI) += sun9i-cci.o
obj-$(CONFIG_MCPM)      += sun9i-setup.o sun9i-mcpm.o
obj-$(CONFIG_PM)        += pm/
obj-$(CONFIG_NET)       += rf/
endif

ifeq ($(CONFIG_SMP), y)
obj-y += sunxi-headsmp.o sunxi-platsmp.o
obj-$(CONFIG_HOTPLUG_CPU) += sunxi-hotplug.o
endif

obj-y += sys_config.o sunxi_dump_reg.o sunxi-chip.o

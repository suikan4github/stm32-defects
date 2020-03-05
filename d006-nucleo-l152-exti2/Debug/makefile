################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Drivers/STM32L1xx_HAL_Driver/Src/subdir.mk
-include Core/Startup/subdir.mk
-include Core/Src/subdir.mk
-include subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

# Add inputs and outputs from these tool invocations to the build variables 
EXECUTABLES += \
nucleo-l152-exti.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
nucleo-l152-exti.list \

OBJCOPY_BIN += \
nucleo-l152-exti.bin \


# All Target
all: nucleo-l152-exti.elf secondary-outputs

# Tool invocations
nucleo-l152-exti.elf: $(OBJS) $(USER_OBJS) /home/takemasa/STM32CubeIDE/workspace_stm32_defect/nucleo-l152-exti/STM32L152RETX_FLASH.ld
	arm-none-eabi-gcc -o "nucleo-l152-exti.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m3 -T"/home/takemasa/STM32CubeIDE/workspace_stm32_defect/nucleo-l152-exti/STM32L152RETX_FLASH.ld" --specs=nosys.specs -Wl,-Map="nucleo-l152-exti.map" -Wl,--gc-sections -static --specs=nano.specs -mfloat-abi=soft -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

nucleo-l152-exti.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "nucleo-l152-exti.list"
	@echo 'Finished building: $@'
	@echo ' '

nucleo-l152-exti.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "nucleo-l152-exti.bin"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) *
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST) $(OBJCOPY_BIN)

.PHONY: all clean dependents
.SECONDARY:

-include ../makefile.targets

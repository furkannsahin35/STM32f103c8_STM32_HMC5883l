################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Startup/subdir.mk
-include Src/subdir.mk
-include Drivers/STM32F1xx_HAL_Driver/Src/subdir.mk
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
ex_i2c_compass.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
ex_i2c_compass.list \

OBJCOPY_HEX += \
ex_i2c_compass.hex \

OBJCOPY_BIN += \
ex_i2c_compass.bin \


# All Target
all: ex_i2c_compass.elf secondary-outputs

# Tool invocations
ex_i2c_compass.elf: $(OBJS) $(USER_OBJS) C:\Users\F\Desktop\stm_ex\ex_i2c_compass\STM32F103C8TX_FLASH.ld
	arm-none-eabi-gcc -o "ex_i2c_compass.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m3 -T"C:\Users\F\Desktop\stm_ex\ex_i2c_compass\STM32F103C8TX_FLASH.ld" --specs=nosys.specs -Wl,-Map="ex_i2c_compass.map" -Wl,--gc-sections -static --specs=nano.specs -mfloat-abi=soft -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

ex_i2c_compass.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "ex_i2c_compass.list"
	@echo 'Finished building: $@'
	@echo ' '

ex_i2c_compass.hex: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O ihex $(EXECUTABLES) "ex_i2c_compass.hex"
	@echo 'Finished building: $@'
	@echo ' '

ex_i2c_compass.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "ex_i2c_compass.bin"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) *
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST) $(OBJCOPY_HEX) $(OBJCOPY_BIN)

.PHONY: all clean dependents
.SECONDARY:

-include ../makefile.targets

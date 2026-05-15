################################################################################
# Automatically-generated file. Do not edit!
# Toolchain: GNU Tools for STM32 (14.3.rel1)
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Drivers/STM32F4xx_HAL_Driver/Src/subdir.mk
-include Core/Startup/subdir.mk
-include Core/Src/subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(S_DEPS)),)
-include $(S_DEPS)
endif
ifneq ($(strip $(S_UPPER_DEPS)),)
-include $(S_UPPER_DEPS)
endif
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

OPTIONAL_TOOL_DEPS := \
$(wildcard ../makefile.defs) \
$(wildcard ../makefile.init) \
$(wildcard ../makefile.targets) \


BUILD_ARTIFACT_NAME := Modulo Físico Proyecto Señales
BUILD_ARTIFACT_EXTENSION := elf
BUILD_ARTIFACT_PREFIX :=
BUILD_ARTIFACT := $(BUILD_ARTIFACT_PREFIX)$(BUILD_ARTIFACT_NAME)$(if $(BUILD_ARTIFACT_EXTENSION),.$(BUILD_ARTIFACT_EXTENSION),)

# Add inputs and outputs from these tool invocations to the build variables 
EXECUTABLES += \
Modulo\ Físico\ Proyecto\ Señales.elf \

MAP_FILES += \
Modulo\ Físico\ Proyecto\ Señales.map \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
Modulo\ Físico\ Proyecto\ Señales.list \


# All Target
all: main-build

# Main-build Target
main-build: Modulo\ Físico\ Proyecto\ Señales.elf secondary-outputs

# Tool invocations
Modulo\ Físico\ Proyecto\ Señales.elf Modulo\ Físico\ Proyecto\ Señales.map: $(OBJS) $(USER_OBJS) C:\Users\razer\OneDrive\Documentos\GitHub\Proyecto-Se-ales\Modulo\ Físico\ Proyecto\ Señales\STM32F446RETX_FLASH.ld makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-gcc -o "Modulo Físico Proyecto Señales.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m4 -T"C:\Users\razer\OneDrive\Documentos\GitHub\Proyecto-Se-ales\Modulo Físico Proyecto Señales\STM32F446RETX_FLASH.ld" --specs=nosys.specs -Wl,-Map="Modulo Físico Proyecto Señales.map" -Wl,--gc-sections -static --specs=nano.specs -mfpu=fpv4-sp-d16 -mfloat-abi=hard -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES) makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

Modulo\ Físico\ Proyecto\ Señales.list: $(EXECUTABLES) makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "Modulo Físico Proyecto Señales.list"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) Modulo\ Físico\ Proyecto\ Señales.elf Modulo\ Físico\ Proyecto\ Señales.list Modulo\ Físico\ Proyecto\ Señales.map Modulo\\ Físico\\ Proyecto\\ Señales.elf default.size.stdout
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST)

fail-specified-linker-script-missing:
	@echo 'Error: Cannot find the specified linker script. Check the linker settings in the build configuration.'
	@exit 2

warn-no-linker-script-specified:
	@echo 'Warning: No linker script specified. Check the linker settings in the build configuration.'

.PHONY: all clean dependents main-build fail-specified-linker-script-missing warn-no-linker-script-specified

-include ../makefile.targets

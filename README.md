# Expander IO Klipper Addon

Allow using I2C IO expanders to be used as inputs for buttons / filament sensors / etc.

Two boards are currently supported: SX1509 and MCP23017.

Sample configuration for the SX1509:
```
[eio_sx1509 expander]
i2c_mcu: mmb
i2c_address: 62
i2c_bus: i2c3_PB3_PB4
interrupt_pin: !mmb:PC15
[filament_switch_sensor gate5]
switch_pin: ^mmu_sx1509_expander:PIN_5
pause_on_runout: False
```

Sample configuration for the MCP23017:
```
[eio_mcp23017 expander]
i2c_mcu: mmb
i2c_address: 32
i2c_bus: i2c3_PB3_PB4
interrupt_pin: !mmb:PC15
[filament_switch_sensor gate3]
switch_pin: ^mmu_mcp23017_expander:PIN_3
pause_on_runout: False
```
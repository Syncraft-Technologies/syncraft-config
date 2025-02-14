# Syncraft X1 - V4

## Klipper Variables file
Include this template in the `~/printer-data/config/variables.cfg` file:

```conf
    [Variables]
    currentextruder = 'extruder'
    machine = 'Syncraft X1'
    material_cura = ''
    material_ext0 = ''
    material_ext1 = 'empty'
    nozzle = ''
    setup_verification = ''
```

## Extra files
Extra configuration needed in the `~/printer-data/config/printer.cfg` file:

```conf
[mcu]
canbus_uuid = <mcu_id>

[mcu rp2040]
canbus_uuid = <mcu_id>
```
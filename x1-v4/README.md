# Syncraft X1 V4

Extra configuration needed at the `~/printer-data/config/printer.cfg` file:

```conf
[mcu]
canbus_uuid = <mcu_id>

[mcu rp2040]
canbus_uuid = <mcu_id>
```

## Moonraker configuration

Include only the local `moonraker.conf`, not `common/extras/moonraker.conf`.
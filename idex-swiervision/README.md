# Syncraft IDEX

Extra configuration needed in the `~/printer-data/config/printer.cfg` file:

```conf
[mcu]
canbus_uuid = <mcu_id>

[mcu rp2040]
canbus_uuid = <mcu_id>
```

## Installing calibration files

Create a symbolic link from the `calibrations` directory to the `~/printer_data/gcodes` directory named as `.calibrations`.

```bash
cd ~
```
```bash
ln -s ~/syncraft-config/idex/calibrations printer_data/gcodes/.calibrations
```

## Moonraker configuration

Do not include `common` moonraker configuration at `moonraker.conf`. Instead just include local:

```conf
[include syncraft-config/<model_name>/extras/moonraker.conf]
```
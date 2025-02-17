# Syncraft config

This repository contains the configuration files for Syncraft 3D printers.

## File structure

Each printer model has its own directory and `.cfg` file, both named after the model.

- Klipper configurations and macros are in the printer model's directory.
	```
	├── printers
	│   └── <model_a>
	│   └── <model_b>
	```
- Shared configurations for multiple models are in root directory.
	```
	├── beds
	│── boards
	├── calibrations
	├── extruders
	├── fans
	├── klipper-sets
	├── lights
	├── macros
	├── sensors
	├── services
	├── step-motors
	└── README.md
	```
## Installation

1. Clone the repository and link it to your Klipper configuration directory:
	```bash
	cd ~
	```
	```bash
	git clone https://github.com/Syncraft-Technologies/syncraft-config.git
	```
	```bash
	ln -s ~/syncraft-config printer_data/config/syncraft-config
	```
2. Include the model's file in your main Klipper configuration (`~/printer_data/config/printer.cfg`):
	```conf
	[include syncraft-config/<model_name>.cfg]
	```
3. Check the model's `README.md` for more instructions.

### Moonraker configuration

Since Moonraker configuration allow includes, you can include the common and specific configuration files in your `~/printer_data/config/moonraker.conf` file:

```conf
[include syncraft-config/printers/<model_name>/extras/moonraker.conf]
```
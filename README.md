# Syncraft config

This repository contains the configuration files for Syncraft 3D printers.

## File structure

Each printer model has its own directory and `.cfg` file, both named after the model.

- Klipper configurations and macros are in the model's directory.
- Non-Klipper configurations are in the model's `extras` subdirectory.
- Shared configurations for multiple models are in the `common` directory.

```
├── common
├── <model_a>
│   ├── extras
│   └── README.md
├── <model_a>.cfg
├── <model_b>
│   ├── extras
│   └── README.md
├── <model_b>.cfg
└── README.md
```

## Installation

1. Clone the repository and link it to your Klipper configuration directory:
	```bash
	cd ~
	git clone https://github.com/Syncraft-Technologies/syncraft-config.git
	ln -s ~/syncraft-config printer_data/config/syncraft-config
	```
2. Include the model's file in your main Klipper configuration (`~/printer_data/config/printer.cfg`):
	```conf
	[include syncraft-config/<model_name>.cfg]
	```
3. Check the model's `README.md` for more instructions.
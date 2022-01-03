# SmartRent Home Assistant Component

[![GitHub](https://img.shields.io/github/license/zacherythomas/homeassistant-smartrent?style=for-the-badge)](LICENSE.txt)
[![hacs_badge](https://img.shields.io/badge/HACS-Custom-41BDF5.svg?style=for-the-badge)](https://github.com/hacs/integration)
[![Code style: black](https://img.shields.io/badge/code%20style-black-000000.svg?style=for-the-badge)](https://github.com/psf/black)


This is a basic Homeassistant component to support SmartRent Locks and Thermostats. This component uses the `smartrent.py` library that can be found [here](https://github.com/ZacheryThomas/smartrent.py)!

## Basic Setup

### Moving custom component to right directory
```
└── ...
└── configuration.yaml
└── secrects.yaml
└── custom_components
    └── smartrent
        └── climate.py
        └── lock.py
        └── manifest.json
        └── ...
```

You have to move all content in the `custom_components/smartrent` directory to the same location in Home Assistant. If a `custom_components` directory does not already exist in your Home Assistant instance, you will have to make one. You can learn more [here](https://developers.home-assistant.io/docs/creating_integration_file_structure#where-home-assistant-looks-for-integrations).

### Restarting HA
After all of those are in place, you can restart your Home Assistant server and the component should load.

### Start the integration
You should be able to now load the integration. This can be done by going to `config -> devices & services -> + ADD INTEGRATION`

You should be able to search for SmartRent and then enter your email and password in the popup.

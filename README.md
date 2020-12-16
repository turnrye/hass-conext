# Home Assistnat Conext SW Sensors

This repository is for pre-made sensor configurations for the Conext SW line of inverter/chargers by Schneider Electric. This was made primarily with the Conext SW4048, but it should be compatible with other SW-line devices.

Today, this just contains sensor data, but in the future lovelace cards will be added.

## Quick start

Clone the repository within your home-assistant working directory:

```sh
git clone https://github.com/turnrye/hass-conext.git
```

Add these two entries to your `configuration.yaml`, modifying the host/port to suit your application.

```yaml
modbus:
- name: combox
  type: tcp
  host: 10.0.10.127
  port: 502
sensor conext: !include hass-conext/conext-sensors.yaml
```

Note that this assumes your conext SW device is on modbus slave address 90; this may or may not be a safe assumption for your use. Use modbus utilities and the combox configuration in order to verify. If necessary, edit the `hass-conxt/conext-sensors.yaml` file to replace 90 with the appropriate address.

## Updating

In order to get the latest-and-greatest, just do a `git pull` within the `hass-conext` directory and restart Home Assistant.

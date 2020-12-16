Add these two entries to your `configuration.yaml`, modifying the host/port to suit your application.

Note that this assumes your conext SW device is on modbus slave address 90; this may or may not be a safe assumption for your use. Use modbus utilities and the combox configuration in order to verify.

```
modbus:
- name: combox
  type: tcp
  host: 10.0.10.127
  port: 502
sensor conext: !include hass-conext/conext-sensors.yaml
```

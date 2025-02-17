# HA Calibrate Zigbee Avatto ZWT-100 Thermostat using Zigbee2MQTT

This blueprint uses external temperature sensor readings and updates the local calibration of selected thermostat so it shows the same temperature with the sensibility of 0.1 degrees.
The termostat sensor must be set to Internal or Both.
If you use ZHA, replace the mqtt service section with:

- service: number.set_value
  target:
    entity_id: "{{ device_calib }}"
  data:
    value: "{{ target_calib_trunc }}"

![Screenshot 2025-02-16 104126](https://github.com/user-attachments/assets/5cb84b6a-e086-4fb0-898d-cb98843ef6fd)

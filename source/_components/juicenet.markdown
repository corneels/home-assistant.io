---
title: "Juicenet"
description: "Instructions on how to setup WiFi-equipped Juicenet charging stations with Home Assistant."
logo: juicenet.png
ha_category:
  - Energy
  - Sensor
ha_release: 0.47
redirect_from:
  - /components/sensor.juicenet/
---

The `juicenet` sensor platform pulls data from a [JuiceNet](https://emotorwerks.com/products/juicenet/) charging station equipped with a wifi connection. It will access and make available all of the devices attached to your account.

## Configuration

To enable the platform in your installation, add the following to your `configuration.yaml` file:

```yaml
# Example configuration.yaml entry
juicenet:
    access_token: ACCESS_TOKEN
```

{% configuration %}
access_token:
  description: "Your eMotorWerks API Token can be found in the [dashboard](https://dashboard.emotorwerks.com/Manage)."
  required: true
  type: string
{% endconfiguration %}

## Sensor

The `juicenet` sensor platform allows you to get data from your [JuiceNet](https://emotorwerks.com/products/juicenet/) sensors.

### Added sensors

These sensors will be added for each juicenet device in your account:

- Status
- Temperature (inside the device)
- Voltage
- Amps
- Watts
- Charge time of session
- Energy added this session
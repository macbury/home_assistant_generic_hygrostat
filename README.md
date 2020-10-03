# Generic hygrostat integration
This PR introduces a new virtual humidifier or dehumidifier device that uses an existing humidity sensor to act as a hygrostat, controlling a switch to turn it on and off as needed to sustain target humidity.

# Manual Installation

Copy `custom_components/generic_hygrostat` to `<config>/custom_components/generic_hygrostat` directory.

# Installation using hacs

You can add this repository to [your hacs](https://hacs.xyz/)

# Home Assistant configuration

``` YAML
generic_hygrostat:
  - name: Bedroom
    humidifier: switch.humidifier_plug
    target_sensor: sensor.outside_humidity
    min_humidity: 30
    max_humidity: 70
    target_humidity: 50
    away_humidity: 40
    away_fixed: True
    sensor_stale_duration: 00:15:00
```


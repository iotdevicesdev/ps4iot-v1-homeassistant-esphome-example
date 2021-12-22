# PS4IoT_V1 Home Assistant with ESPHome setup example
PS4IoT_V1 Smart Power Supply Unit Module is tested under Home Assistant server with ESPHome plugin specially deployed test environment. The PS4IoT_V1 demo setup is placed in "managed by MCU mode" using ESP8266 as the MCU.

Hackaday Project Page: https://hackaday.io/project/183099-ps4iotv1-smart-power-supply-unit-module


![PS4IoT_V1 Ports](https://github.com/iotdevicesdev/ps4iot-v1-homeassistant-esphome-example/blob/main/PS4IoT_V1_Quick_Facts_Sheet_Ports.jpg)


## What's in example files

To enable the module in its full capacity, you need to create a yaml configuration script in ESPHome.

- nodemcu-ps4iot-v1.yaml - contains ESPHome node-side configuration script example

In addition, you must add a synthetic battery voltage rate sensor to the Home Assistant server's general
'configuration.yaml' configuration file:

- configuration.yaml - contains Home Assitant server-side configuration script example

## PS4IoT in managed by MCU mode setup example

![Managed mode setup example](https://github.com/iotdevicesdev/ps4iot-v1-homeassistant-esphome-example/blob/main/PS4IoT_V1_Quick_Facts_Sheet_ManagedMode-SetupExample.jpg)

### Node-side (ESPHome plugin node config) entities:

The configuration must include the following entities:
- sensor.nodemcu_battery_voltage_level
- sensor.battery_voltage_change_per_hour
- binary_sensor.nodemcu_ps4iot_external_power_supply_detector
- switch.nodemcu_ps4iot_bat_charge_enable
- binary_sensor.nodemcu_ps4iot_red_charge_in_progress
- binary_sensor.nodemcu_ps4iot_blue_charge_completed


### Server-side (Home Assistant general config) entities:
- sensor.battery_voltage_change_per_hour
#### Additional server-sided text state sensors:
- sensor.nodemcu_ps4iot_battery_level_text_state
- sensor.nodemcu_ps4iot_charge_text_state
- sensor.nodemcu_ps4iot_numeric_battery_level_value

## Install

1. Download .yaml example files
2. Under ESPHome plugin menu in your Home Assistant Server instance create new ESP8266 or ESP32 node. 
3. Make all needed modifications and additions to your node's yaml-file.
4. Compile and use
5. Also you may add server-aided additional state sensors using configuration.yaml file as in examples.

## Resulting Home Assistant dashboard basic widget example
![HA Dashboard Widget](https://github.com/iotdevicesdev/ps4iot-v1-homeassistant-esphome-example/blob/main/PS4IoT_V1_Main_States_Widget_HA_Dashboard_SetupExample.jpg)

## Buy PS4IoT_V1 Smart Power Supply Unit Module: 

On Tindie: https://www.tindie.com/products/iotdev/ps4iot-smart-power-supply-unit-module/

IoT-devices Online Shop: https://iot-devices.com.ua/en/

## Watch PS4IoT_V1 under Home Assistant / ESPHome demo video

<a href="https://www.youtube.com/watch?feature=player_embedded&v=rUE2VASIHns" target="_blank">
 <img src="https://img.youtube.com/vi/rUE2VASIHns/mqdefault.jpg" alt="Watch the video" border="10" />
</a>

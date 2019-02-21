# Custom components for Home Assistant
## Broadlink IR Climate Component is obsolete. [Go to the new version](https://github.com/smartHomeHub/SmartIR) (HA 0.88 and earlier)

## Broadlink IR Media Player Component is obsolete. [Go to the new version](https://github.com/smartHomeHub/SmartIR) (HA 0.88 and earlier)


## Broadlink RF Fan

#### Configuration variables:
**name** (Optional): Name of fan component<br />
**host** (Required): The hostname/IP address of the broadlink rm device<br />
**mac** (Required): The MAC address of the broadlink rm device<br />
**timeout** (Optional): Timeout in seconds for the connection to the device<br />
**rfcodes_ini** (Required): The path of RF codes ini file<br />
**default_speed** (Optional): Default fan speed when fan is turned on<br />
**default_direction** (Optional): Default fan rotation direction when turned on. Possible values are right (clockwise) and left (anti-clockwise). (default: left)<br />
**customize** (Optional): List of options to customize.<br />
  **- speeds** (Optional*): List of supported speeds (default: low, medium, high)<br />

#### Example:
```yaml
fan:
  - platform: broadlink
    name: Living Room Fan
    host: 192.168.1.85
    mac: 'BB:BB:BB:BB:BB:BB'
    rfcodes_ini: 'broadlink_fan_codes/living_room_fan.ini'
    default_speed: low
    defaut_direction: left
    customize:
        speeds:
            - low
            - medium
            - high
            - highest
```

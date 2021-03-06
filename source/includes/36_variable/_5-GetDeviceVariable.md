## GetDeviceVariable

Function called by a DriverWorks driver to get the value of another device's variable. This API should not be invoked during OnDriverInit.

###### Available from 1.6.0.


### Signature

`C4:GetDeviceVariable(idDevice, idVariable)`	


| Parameter | Description |
| --- | --- |
| num | Device ID of the device that owns the specified variable |
| num | Variable ID of the specified variable |


### Returns

| Returns | Description |
| --- | --- |
| str |  String Value of the requested variable, nil if not found. |


### Usage Note

User Variables belong to the Variable Agent, with a DeviceID of 100001.


### Examples

Gets and prints the value of the HVAC mode and temperature variables of a Control4 Thermostat registered in the project as Device ID 84:

```lua
print(C4:GetDeviceVariable(84, 1000))
print(C4:GetDeviceVariable(84, 1003))
```

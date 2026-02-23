
# Astarte Interfaces

## io.edgehog.devicemanager.BaseImage v0.1



### About

This interface is of type `properties` and is owned by the `device`, meaning that it is the device which initiates the data flow.
Thanks to this type of interface, the device can set a persistent, stateful, synchronized state with no concept of history or timestamping.


### Mappings

The interface has the following mappings:

- `/fingerprint` with `string` type. OS bundle release identification code
- `/name` with `string` type. Name of the bundle
- `/version` with `string` type. Version of the bundle
- `/buildId` with `string` type. Human readable build identifier. Examples are `[date][time]` or `[date]-[time]-[git-commit]`


### `/fingerprint`

OS bundle release identification code



This endpoint accepts values of type `string`: an UTF-8 string, at most 65536 bytes long.

The value of the property cannot be unset.

### `/name`

Name of the bundle



This endpoint accepts values of type `string`: an UTF-8 string, at most 65536 bytes long.

The value of the property cannot be unset.

### `/version`

Version of the bundle



This endpoint accepts values of type `string`: an UTF-8 string, at most 65536 bytes long.

The value of the property cannot be unset.

### `/buildId`

Human readable build identifier. Examples are `[date][time]` or `[date]-[time]-[git-commit]`



This endpoint accepts values of type `string`: an UTF-8 string, at most 65536 bytes long.

The value of the property cannot be unset.


## io.edgehog.devicemanager.BatteryStatus v0.1



### About

This interface is of type `datastream` and is owned by the `device`, meaning that it is the device which initiates the data flow.
Thanks to this type of interface, the device can send a mutable, ordered stream of data, with no concept of persistent state or synchronization.

Data gets sent with an `object` aggregation.
Astarte expects the owner to send all of the interface's mappings at the same time, packed in a single message.

### Mappings

The interface has the following mappings:

- `/%{battery_slot}/levelPercentage` with `double` type. Battery level estimated percentage [0.0%-100.0%]
- `/%{battery_slot}/levelAbsoluteError` with `double` type. Battery level measurement absolute error [0.0-100.0]
- `/%{battery_slot}/status` with `string` type. Battery status string, any of: Charging, Discharging, Idle, EitherIdleOrCharging, Failure, Removed, Unknown


### `/%{battery_slot}/levelPercentage`

Battery level estimated percentage [0.0%-100.0%]



This endpoint accepts values of type `double`: a double-precision floating-point number as specified by binary64, by the IEEE 754 standard.

The endpoint is parametric and `battery_slot` can be replaced with any valid string to send data on specialized paths.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Astarte expects a valid timestamp to be attached each time data is produced.
Data is considered delivered when the transport successfully sends the data regardless of the outcome.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 5184000 seconds before it is erased from the database.

### `/%{battery_slot}/levelAbsoluteError`

Battery level measurement absolute error [0.0-100.0]



This endpoint accepts values of type `double`: a double-precision floating-point number as specified by binary64, by the IEEE 754 standard.

The endpoint is parametric and `battery_slot` can be replaced with any valid string to send data on specialized paths.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Astarte expects a valid timestamp to be attached each time data is produced.
Data is considered delivered when the transport successfully sends the data regardless of the outcome.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 5184000 seconds before it is erased from the database.

### `/%{battery_slot}/status`

Battery status string, any of: Charging, Discharging, Idle, EitherIdleOrCharging, Failure, Removed, Unknown



This endpoint accepts values of type `string`: an UTF-8 string, at most 65536 bytes long.

The endpoint is parametric and `battery_slot` can be replaced with any valid string to send data on specialized paths.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Astarte expects a valid timestamp to be attached each time data is produced.
Data is considered delivered when the transport successfully sends the data regardless of the outcome.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 5184000 seconds before it is erased from the database.


## io.edgehog.devicemanager.CellularConnectionProperties v0.1



### About

This interface is of type `properties` and is owned by the `device`, meaning that it is the device which initiates the data flow.
Thanks to this type of interface, the device can set a persistent, stateful, synchronized state with no concept of history or timestamping.


### Mappings

The interface has the following mappings:

- `/%{id}/apn` with `string` type. Operator apn address.
- `/%{id}/imei` with `string` type. The modem IMEI code of the device.
- `/%{id}/imsi` with `string` type. The SIM IMSI code of the device.


### `/%{id}/apn`

Operator apn address.



This endpoint accepts values of type `string`: an UTF-8 string, at most 65536 bytes long.

The endpoint is parametric and `id` can be replaced with any valid string to send data on specialized paths.

The value of the property can be unset.

### `/%{id}/imei`

The modem IMEI code of the device.



This endpoint accepts values of type `string`: an UTF-8 string, at most 65536 bytes long.

The endpoint is parametric and `id` can be replaced with any valid string to send data on specialized paths.

The value of the property can be unset.

### `/%{id}/imsi`

The SIM IMSI code of the device.



This endpoint accepts values of type `string`: an UTF-8 string, at most 65536 bytes long.

The endpoint is parametric and `id` can be replaced with any valid string to send data on specialized paths.

The value of the property can be unset.


## io.edgehog.devicemanager.CellularConnectionStatus v0.1



### About

This interface is of type `datastream` and is owned by the `device`, meaning that it is the device which initiates the data flow.
Thanks to this type of interface, the device can send a mutable, ordered stream of data, with no concept of persistent state or synchronization.

Data gets sent with an `object` aggregation.
Astarte expects the owner to send all of the interface's mappings at the same time, packed in a single message.

### Mappings

The interface has the following mappings:

- `/%{id}/carrier` with `string` type. Connectivity carrier operator name.
- `/%{id}/cellId` with `longinteger` type. The Cell ID in hexadecimal format, either 16 bit for 2G or 28 bit for 3G or 4G.
- `/%{id}/mobileCountryCode` with `integer` type. The mobile country code (MCC) for the device's home network. Valid range: 0–999.
- `/%{id}/mobileNetworkCode` with `integer` type. The Mobile Network Code for the device's home network. This is the MNC for GSM, WCDMA, LTE and NR. CDMA uses the System ID (SID). Valid range for MNC: 0–999. Valid range for SID: 0–32767.
- `/%{id}/localAreaCode` with `integer` type. Two byte location area code in hexadecimal format.
- `/%{id}/registrationStatus` with `string` type. GSM/LTE registration status. Possible values: [NotRegistered, Registered, SearchingOperator, RegistrationDenied, Unknown, RegisteredRoaming]
- `/%{id}/rssi` with `double` type. Signal strenght of the device in dBm.
- `/%{id}/technology` with `string` type. Access Technology. Possible values [GSM, GSMCompact, UTRAN, GSMwEGPRS, UTRANwHSDPA, UTRANwHSUPA, UTRANwHSDPAandHSUPA, EUTRAN]


### `/%{id}/carrier`

Connectivity carrier operator name.



This endpoint accepts values of type `string`: an UTF-8 string, at most 65536 bytes long.

The endpoint is parametric and `id` can be replaced with any valid string to send data on specialized paths.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Astarte expects a valid timestamp to be attached each time data is produced.
Data is considered delivered when the transport successfully sends the data regardless of the outcome.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 5184000 seconds before it is erased from the database.

### `/%{id}/cellId`

The Cell ID in hexadecimal format, either 16 bit for 2G or 28 bit for 3G or 4G.



This endpoint accepts values of type `longinteger`: a signed 64 bit integer (please note that longinteger is represented as a string by default in JSON-based APIs.).

The endpoint is parametric and `id` can be replaced with any valid string to send data on specialized paths.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Astarte expects a valid timestamp to be attached each time data is produced.
Data is considered delivered when the transport successfully sends the data regardless of the outcome.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 5184000 seconds before it is erased from the database.

### `/%{id}/mobileCountryCode`

The mobile country code (MCC) for the device's home network. Valid range: 0–999.



This endpoint accepts values of type `integer`: a signed 32 bit integer.

The endpoint is parametric and `id` can be replaced with any valid string to send data on specialized paths.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Astarte expects a valid timestamp to be attached each time data is produced.
Data is considered delivered when the transport successfully sends the data regardless of the outcome.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 5184000 seconds before it is erased from the database.

### `/%{id}/mobileNetworkCode`

The Mobile Network Code for the device's home network. This is the MNC for GSM, WCDMA, LTE and NR. CDMA uses the System ID (SID). Valid range for MNC: 0–999. Valid range for SID: 0–32767.



This endpoint accepts values of type `integer`: a signed 32 bit integer.

The endpoint is parametric and `id` can be replaced with any valid string to send data on specialized paths.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Astarte expects a valid timestamp to be attached each time data is produced.
Data is considered delivered when the transport successfully sends the data regardless of the outcome.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 5184000 seconds before it is erased from the database.

### `/%{id}/localAreaCode`

Two byte location area code in hexadecimal format.



This endpoint accepts values of type `integer`: a signed 32 bit integer.

The endpoint is parametric and `id` can be replaced with any valid string to send data on specialized paths.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Astarte expects a valid timestamp to be attached each time data is produced.
Data is considered delivered when the transport successfully sends the data regardless of the outcome.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 5184000 seconds before it is erased from the database.

### `/%{id}/registrationStatus`

GSM/LTE registration status. Possible values: [NotRegistered, Registered, SearchingOperator, RegistrationDenied, Unknown, RegisteredRoaming]



This endpoint accepts values of type `string`: an UTF-8 string, at most 65536 bytes long.

The endpoint is parametric and `id` can be replaced with any valid string to send data on specialized paths.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Astarte expects a valid timestamp to be attached each time data is produced.
Data is considered delivered when the transport successfully sends the data regardless of the outcome.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 5184000 seconds before it is erased from the database.

### `/%{id}/rssi`

Signal strenght of the device in dBm.



This endpoint accepts values of type `double`: a double-precision floating-point number as specified by binary64, by the IEEE 754 standard.

The endpoint is parametric and `id` can be replaced with any valid string to send data on specialized paths.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Astarte expects a valid timestamp to be attached each time data is produced.
Data is considered delivered when the transport successfully sends the data regardless of the outcome.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 5184000 seconds before it is erased from the database.

### `/%{id}/technology`

Access Technology. Possible values [GSM, GSMCompact, UTRAN, GSMwEGPRS, UTRANwHSDPA, UTRANwHSUPA, UTRANwHSDPAandHSUPA, EUTRAN]



This endpoint accepts values of type `string`: an UTF-8 string, at most 65536 bytes long.

The endpoint is parametric and `id` can be replaced with any valid string to send data on specialized paths.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Astarte expects a valid timestamp to be attached each time data is produced.
Data is considered delivered when the transport successfully sends the data regardless of the outcome.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 5184000 seconds before it is erased from the database.


## io.edgehog.devicemanager.Commands v0.1



### About

This interface is of type `datastream` and is owned by the `server`, meaning that it is the server which initiates the data flow.
Thanks to this type of interface, the server can send a mutable, ordered stream of data, with no concept of persistent state or synchronization.

Data gets sent with an `individual` aggregation.
Each mapping is treated as an independent value and is managed individually.

### Mappings

The interface has the following mappings:

- `/request` with `string` type. Command request. Possible values  ['Reboot']


### `/request`

Command request. Possible values  ['Reboot']



This endpoint accepts values of type `string`: an UTF-8 string, at most 65536 bytes long.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Astarte expects a valid timestamp to be attached each time data is produced.
Data is considered delivered when it has been received exactly once by the recipient.
Data is discarded if the transport is temporarily uncapable of delivering it.


## io.edgehog.devicemanager.ForwarderSessionRequest v0.1

Configuration to open a session with the Edgehog Forwarder from a device to a certain host.

### About

This interface is of type `datastream` and is owned by the `server`, meaning that it is the server which initiates the data flow.
Thanks to this type of interface, the server can send a mutable, ordered stream of data, with no concept of persistent state or synchronization.

Data gets sent with an `object` aggregation.
Astarte expects the owner to send all of the interface's mappings at the same time, packed in a single message.

### Mappings

The interface has the following mappings:

- `/request/session_token` with `string` type. The session token thanks to which the device can authenticates itself through Edgehog.
- `/request/port` with `integer` type. The host port the device must connect to.
- `/request/host` with `string` type. The IP address or host name the device must connect to.
- `/request/secure` with `boolean` type. Indicates whether the connection should use TLS, i.e. 'ws' or 'wss' scheme.


### `/request/session_token`

The session token thanks to which the device can authenticates itself through Edgehog.



This endpoint accepts values of type `string`: an UTF-8 string, at most 65536 bytes long.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Data is considered delivered when the transport successfully sends the data regardless of the outcome.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 31556952 seconds before it is erased from the database.

### `/request/port`

The host port the device must connect to.



This endpoint accepts values of type `integer`: a signed 32 bit integer.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Data is considered delivered when the transport successfully sends the data regardless of the outcome.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 31556952 seconds before it is erased from the database.

### `/request/host`

The IP address or host name the device must connect to.



This endpoint accepts values of type `string`: an UTF-8 string, at most 65536 bytes long.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Data is considered delivered when the transport successfully sends the data regardless of the outcome.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 31556952 seconds before it is erased from the database.

### `/request/secure`

Indicates whether the connection should use TLS, i.e. 'ws' or 'wss' scheme.



This endpoint accepts values of type `boolean`: either true or false, adhering to JSON boolean type.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Data is considered delivered when the transport successfully sends the data regardless of the outcome.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 31556952 seconds before it is erased from the database.


## io.edgehog.devicemanager.ForwarderSessionState v0.1

Information provided by the device about the status of a forwarder session.

### About

This interface is of type `properties` and is owned by the `device`, meaning that it is the device which initiates the data flow.
Thanks to this type of interface, the device can set a persistent, stateful, synchronized state with no concept of history or timestamping.


### Mappings

The interface has the following mappings:

- `/%{session_token}/status` with `string` type. Indicates if the device is connecting, or connected to a forwarder session.


### `/%{session_token}/status`

Indicates if the device is connecting, or connected to a forwarder session.

An enum with the following possible values: Connecting | Connected.

This endpoint accepts values of type `string`: an UTF-8 string, at most 65536 bytes long.

The endpoint is parametric and `session_token` can be replaced with any valid string to send data on specialized paths.

The value of the property can be unset.


## io.edgehog.devicemanager.Geolocation v0.1

Generic Geolocation sampled data.

Geolocation allows geolocation sensors to stream location data, such as GPS data. Values availability depends on what sensors are present on devices and what measurement systems are in use. The id represents a unique identifier for an individual sensor.

### About

This interface is of type `datastream` and is owned by the `device`, meaning that it is the device which initiates the data flow.
Thanks to this type of interface, the device can send a mutable, ordered stream of data, with no concept of persistent state or synchronization.

Data gets sent with an `object` aggregation.
Astarte expects the owner to send all of the interface's mappings at the same time, packed in a single message.

### Mappings

The interface has the following mappings:

- `/%{id}/latitude` with `double` type. Sampled latitude value.
- `/%{id}/longitude` with `double` type. Sampled longitude value.
- `/%{id}/altitude` with `double` type. Sampled altitude value.
- `/%{id}/accuracy` with `double` type. Sampled accuracy of the latitude and longitude properties.
- `/%{id}/altitudeAccuracy` with `double` type. Sampled accuracy of the altitude property.
- `/%{id}/heading` with `double` type. Sampled value representing the direction towards which the device is facing.
- `/%{id}/speed` with `double` type. Sampled value representing the velocity of the device.


### `/%{id}/latitude`

Sampled latitude value.



This endpoint accepts values of type `double`: a double-precision floating-point number as specified by binary64, by the IEEE 754 standard.

The endpoint is parametric and `id` can be replaced with any valid string to send data on specialized paths.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Astarte expects a valid timestamp to be attached each time data is produced.
Data is considered delivered when the transport successfully sends the data regardless of the outcome.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 5184000 seconds before it is erased from the database.

### `/%{id}/longitude`

Sampled longitude value.



This endpoint accepts values of type `double`: a double-precision floating-point number as specified by binary64, by the IEEE 754 standard.

The endpoint is parametric and `id` can be replaced with any valid string to send data on specialized paths.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Astarte expects a valid timestamp to be attached each time data is produced.
Data is considered delivered when the transport successfully sends the data regardless of the outcome.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 5184000 seconds before it is erased from the database.

### `/%{id}/altitude`

Sampled altitude value.



This endpoint accepts values of type `double`: a double-precision floating-point number as specified by binary64, by the IEEE 754 standard.

The endpoint is parametric and `id` can be replaced with any valid string to send data on specialized paths.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Astarte expects a valid timestamp to be attached each time data is produced.
Data is considered delivered when the transport successfully sends the data regardless of the outcome.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 5184000 seconds before it is erased from the database.

### `/%{id}/accuracy`

Sampled accuracy of the latitude and longitude properties.



This endpoint accepts values of type `double`: a double-precision floating-point number as specified by binary64, by the IEEE 754 standard.

The endpoint is parametric and `id` can be replaced with any valid string to send data on specialized paths.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Astarte expects a valid timestamp to be attached each time data is produced.
Data is considered delivered when the transport successfully sends the data regardless of the outcome.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 5184000 seconds before it is erased from the database.

### `/%{id}/altitudeAccuracy`

Sampled accuracy of the altitude property.



This endpoint accepts values of type `double`: a double-precision floating-point number as specified by binary64, by the IEEE 754 standard.

The endpoint is parametric and `id` can be replaced with any valid string to send data on specialized paths.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Astarte expects a valid timestamp to be attached each time data is produced.
Data is considered delivered when the transport successfully sends the data regardless of the outcome.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 5184000 seconds before it is erased from the database.

### `/%{id}/heading`

Sampled value representing the direction towards which the device is facing.



This endpoint accepts values of type `double`: a double-precision floating-point number as specified by binary64, by the IEEE 754 standard.

The endpoint is parametric and `id` can be replaced with any valid string to send data on specialized paths.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Astarte expects a valid timestamp to be attached each time data is produced.
Data is considered delivered when the transport successfully sends the data regardless of the outcome.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 5184000 seconds before it is erased from the database.

### `/%{id}/speed`

Sampled value representing the velocity of the device.



This endpoint accepts values of type `double`: a double-precision floating-point number as specified by binary64, by the IEEE 754 standard.

The endpoint is parametric and `id` can be replaced with any valid string to send data on specialized paths.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Astarte expects a valid timestamp to be attached each time data is produced.
Data is considered delivered when the transport successfully sends the data regardless of the outcome.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 5184000 seconds before it is erased from the database.


## io.edgehog.devicemanager.HardwareInfo v0.1

General hardware capabilities

### About

This interface is of type `properties` and is owned by the `device`, meaning that it is the device which initiates the data flow.
Thanks to this type of interface, the device can set a persistent, stateful, synchronized state with no concept of history or timestamping.


### Mappings

The interface has the following mappings:

- `/cpu/architecture` with `string` type. CPU Architecture 
- `/cpu/model` with `string` type. CPU Model Code
- `/cpu/modelName` with `string` type. CPU Model Display Name
- `/cpu/vendor` with `string` type. CPU Vendor
- `/mem/totalBytes` with `longinteger` type. Total RAM quantity (Bytes)


### `/cpu/architecture`

CPU Architecture 



This endpoint accepts values of type `string`: an UTF-8 string, at most 65536 bytes long.

The value of the property cannot be unset.

### `/cpu/model`

CPU Model Code



This endpoint accepts values of type `string`: an UTF-8 string, at most 65536 bytes long.

The value of the property cannot be unset.

### `/cpu/modelName`

CPU Model Display Name



This endpoint accepts values of type `string`: an UTF-8 string, at most 65536 bytes long.

The value of the property cannot be unset.

### `/cpu/vendor`

CPU Vendor



This endpoint accepts values of type `string`: an UTF-8 string, at most 65536 bytes long.

The value of the property cannot be unset.

### `/mem/totalBytes`

Total RAM quantity (Bytes)



This endpoint accepts values of type `longinteger`: a signed 64 bit integer (please note that longinteger is represented as a string by default in JSON-based APIs.).

The value of the property cannot be unset.


## io.edgehog.devicemanager.LedBehavior v0.1



### About

This interface is of type `datastream` and is owned by the `server`, meaning that it is the server which initiates the data flow.
Thanks to this type of interface, the server can send a mutable, ordered stream of data, with no concept of persistent state or synchronization.

Data gets sent with an `individual` aggregation.
Each mapping is treated as an independent value and is managed individually.

### Mappings

The interface has the following mappings:

- `/%{led_id}/behavior` with `string` type. Enum describing the behavior of the given led. Possible values: [Blink60Seconds | DoubleBlink60Seconds | SlowBlink60Seconds]


### `/%{led_id}/behavior`

Enum describing the behavior of the given led. Possible values: [Blink60Seconds | DoubleBlink60Seconds | SlowBlink60Seconds]

Blink60Seconds: Blinking
DoubleBlink60Seconds: Double blinking
SlowBlink60Seconds: Slow blinking

This endpoint accepts values of type `string`: an UTF-8 string, at most 65536 bytes long.

The endpoint is parametric and `led_id` can be replaced with any valid string to send data on specialized paths.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Data is considered delivered when it has been received exactly once by the recipient.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 5184000 seconds before it is erased from the database.


## io.edgehog.devicemanager.NetworkInterfaceProperties v0.1



### About

This interface is of type `properties` and is owned by the `device`, meaning that it is the device which initiates the data flow.
Thanks to this type of interface, the device can set a persistent, stateful, synchronized state with no concept of history or timestamping.


### Mappings

The interface has the following mappings:

- `/%{iface_name}/macAddress` with `string` type. Normalized physical address. Example value is "00:aa:bb:cc:dd:ee" (always lower case)
- `/%{iface_name}/technologyType` with `string` type. Connection technology. Possible values: [Ethernet, Bluetooth, Cellular, WiFi]


### `/%{iface_name}/macAddress`

Normalized physical address. Example value is "00:aa:bb:cc:dd:ee" (always lower case)



This endpoint accepts values of type `string`: an UTF-8 string, at most 65536 bytes long.

The endpoint is parametric and `iface_name` can be replaced with any valid string to send data on specialized paths.

The value of the property can be unset.

### `/%{iface_name}/technologyType`

Connection technology. Possible values: [Ethernet, Bluetooth, Cellular, WiFi]



This endpoint accepts values of type `string`: an UTF-8 string, at most 65536 bytes long.

The endpoint is parametric and `iface_name` can be replaced with any valid string to send data on specialized paths.

The value of the property can be unset.


## io.edgehog.devicemanager.OSInfo v0.1



### About

This interface is of type `properties` and is owned by the `device`, meaning that it is the device which initiates the data flow.
Thanks to this type of interface, the device can set a persistent, stateful, synchronized state with no concept of history or timestamping.


### Mappings

The interface has the following mappings:

- `/osName` with `string` type. Name of the Operating System
- `/osVersion` with `string` type. Version of the Operating System


### `/osName`

Name of the Operating System



This endpoint accepts values of type `string`: an UTF-8 string, at most 65536 bytes long.

The value of the property cannot be unset.

### `/osVersion`

Version of the Operating System



This endpoint accepts values of type `string`: an UTF-8 string, at most 65536 bytes long.

The value of the property cannot be unset.


## io.edgehog.devicemanager.OTAEvent v0.1

OTA Events sampled data.

Allows to stream OTA Events data, including OTA Update status, its progress, code and internal message.

### About

This interface is of type `datastream` and is owned by the `device`, meaning that it is the device which initiates the data flow.
Thanks to this type of interface, the device can send a mutable, ordered stream of data, with no concept of persistent state or synchronization.

Data gets sent with an `object` aggregation.
Astarte expects the owner to send all of the interface's mappings at the same time, packed in a single message.

### Mappings

The interface has the following mappings:

- `/event/requestUUID` with `string` type. OTA Request identifier.
- `/event/status` with `string` type. OTA Update status.
- `/event/statusProgress` with `integer` type. Current OTA Update status progress percentage [0%-100%].
- `/event/statusCode` with `string` type. Status code expands OTA Update status with additional information.
- `/event/message` with `string` type. Contains internal message for status code or empty string otherwise.


### `/event/requestUUID`

OTA Request identifier.



This endpoint accepts values of type `string`: an UTF-8 string, at most 65536 bytes long.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Astarte expects a valid timestamp to be attached each time data is produced.
Data is considered delivered when it has been received exactly once by the recipient.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 31556952 seconds before it is erased from the database.

### `/event/status`

OTA Update status.

Value is one of the following strings:

 - `Acknowledged`: the device received an OTA Request.
 - `Downloading`: an update is in the process of downloading.
 - `Deploying`: an update is in the process of deploying.
 - `Deployed`: an update deployed on the device.
 - `Rebooting`: the device is in the process of rebooting.
 - `Success`: an update succeeded. This is a final status of OTA Update.
 - `Error`: an error happened during the update. Also this status can be used to notify about handled errors.
 - `Failure`: an update failed. This is a final status of OTA Update.

This endpoint accepts values of type `string`: an UTF-8 string, at most 65536 bytes long.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Astarte expects a valid timestamp to be attached each time data is produced.
Data is considered delivered when it has been received exactly once by the recipient.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 31556952 seconds before it is erased from the database.

### `/event/statusProgress`

Current OTA Update status progress percentage [0%-100%].

Every OTA Update status has own progress that starts from 0 and ends at 100, for example (pairs of `"status, progress"`): `"Downloading, 0"`, `"Downloading, 50"`, `"Downloading, 100"`, `"Deploying, 10"`, etc.

This endpoint accepts values of type `integer`: a signed 32 bit integer.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Astarte expects a valid timestamp to be attached each time data is produced.
Data is considered delivered when it has been received exactly once by the recipient.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 31556952 seconds before it is erased from the database.

### `/event/statusCode`

Status code expands OTA Update status with additional information.

Some common status codes are:

  - `InvalidRequest`: an update request contains incorrect data.
 - `UpdateAlreadyInProgress`: another update is currently in progress.
  - `NetworkError`: a network error happened during the update.
  - `IOError`: a filesystem error happened during the update.
  - `InternalError`: an internal error happened during the update.
  - `InvalidBaseImage`: an update failed to apply due to an invalid base image.
  - `SystemRollback`: a system rollback has occurred.
  - `Canceled`: an update was canceled.

This endpoint accepts values of type `string`: an UTF-8 string, at most 65536 bytes long.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Astarte expects a valid timestamp to be attached each time data is produced.
Data is considered delivered when it has been received exactly once by the recipient.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 31556952 seconds before it is erased from the database.

### `/event/message`

Contains internal message for status code or empty string otherwise.



This endpoint accepts values of type `string`: an UTF-8 string, at most 65536 bytes long.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Astarte expects a valid timestamp to be attached each time data is produced.
Data is considered delivered when it has been received exactly once by the recipient.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 31556952 seconds before it is erased from the database.


## io.edgehog.devicemanager.OTARequest v1.0



### About

This interface is of type `datastream` and is owned by the `server`, meaning that it is the server which initiates the data flow.
Thanks to this type of interface, the server can send a mutable, ordered stream of data, with no concept of persistent state or synchronization.

Data gets sent with an `object` aggregation.
Astarte expects the owner to send all of the interface's mappings at the same time, packed in a single message.

### Mappings

The interface has the following mappings:

- `/request/operation` with `string` type. OTA Request operation
- `/request/url` with `string` type. File URL
- `/request/uuid` with `string` type. Request identifier


### `/request/operation`

OTA Request operation

Value is one of the following strings:

 - `Update`: push an OTA update operation.
 - `Cancel`: cancel an OTA update if it can still be cancelled.

This endpoint accepts values of type `string`: an UTF-8 string, at most 65536 bytes long.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Data is considered delivered when the transport successfully sends the data regardless of the outcome.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 31556952 seconds before it is erased from the database.

### `/request/url`

File URL

If the operation is Update, this will contain the URL that can be used to download the Update.
 If the operation is Cancel, this will be an empty string.
 Note that the URL will be valid only until the OTA update is active (i.e. it didn't reach a Failure or Success state), after that it's possible that the URL can become invalid.

This endpoint accepts values of type `string`: an UTF-8 string, at most 65536 bytes long.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Data is considered delivered when the transport successfully sends the data regardless of the outcome.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 31556952 seconds before it is erased from the database.

### `/request/uuid`

Request identifier

A UUID that uniquely identifies the OTA request. It must be stored when receiving an Update operation so that it can be matched against in case a Cancel operation is received.

This endpoint accepts values of type `string`: an UTF-8 string, at most 65536 bytes long.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Data is considered delivered when the transport successfully sends the data regardless of the outcome.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 31556952 seconds before it is erased from the database.


## io.edgehog.devicemanager.RuntimeInfo v0.1



### About

This interface is of type `properties` and is owned by the `device`, meaning that it is the device which initiates the data flow.
Thanks to this type of interface, the device can set a persistent, stateful, synchronized state with no concept of history or timestamping.


### Mappings

The interface has the following mappings:

- `/name` with `string` type. Name of the Edgehog runtime. Example value: `edgehog-esp32-device`
- `/url` with `string` type. URL that uniquely identifies the Edgehog Edgehog runtime implementation. Example value: `https://github.com/edgehog-device-manager/edgehog-esp32-device`.
- `/version` with `string` type. Version of the Edgehog runtime. Example value: `0.5`
- `/environment` with `string` type. Environment of the Edgehog runtime. Example value: `esp-idf VERSION`, `Rust 1.58` or `Java 8`


### `/name`

Name of the Edgehog runtime. Example value: `edgehog-esp32-device`



This endpoint accepts values of type `string`: an UTF-8 string, at most 65536 bytes long.

The value of the property cannot be unset.

### `/url`

URL that uniquely identifies the Edgehog Edgehog runtime implementation. Example value: `https://github.com/edgehog-device-manager/edgehog-esp32-device`.



This endpoint accepts values of type `string`: an UTF-8 string, at most 65536 bytes long.

The value of the property cannot be unset.

### `/version`

Version of the Edgehog runtime. Example value: `0.5`



This endpoint accepts values of type `string`: an UTF-8 string, at most 65536 bytes long.

The value of the property cannot be unset.

### `/environment`

Environment of the Edgehog runtime. Example value: `esp-idf VERSION`, `Rust 1.58` or `Java 8`



This endpoint accepts values of type `string`: an UTF-8 string, at most 65536 bytes long.

The value of the property cannot be unset.


## io.edgehog.devicemanager.StorageUsage v0.1



### About

This interface is of type `datastream` and is owned by the `device`, meaning that it is the device which initiates the data flow.
Thanks to this type of interface, the device can send a mutable, ordered stream of data, with no concept of persistent state or synchronization.

Data gets sent with an `object` aggregation.
Astarte expects the owner to send all of the interface's mappings at the same time, packed in a single message.

### Mappings

The interface has the following mappings:

- `/%{label}/totalBytes` with `longinteger` type. Total storage size in bytes
- `/%{label}/freeBytes` with `longinteger` type. Available storage bytes


### `/%{label}/totalBytes`

Total storage size in bytes



This endpoint accepts values of type `longinteger`: a signed 64 bit integer (please note that longinteger is represented as a string by default in JSON-based APIs.).

The endpoint is parametric and `label` can be replaced with any valid string to send data on specialized paths.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Astarte expects a valid timestamp to be attached each time data is produced.
Data is considered delivered when the transport successfully sends the data regardless of the outcome.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 5184000 seconds before it is erased from the database.

### `/%{label}/freeBytes`

Available storage bytes



This endpoint accepts values of type `longinteger`: a signed 64 bit integer (please note that longinteger is represented as a string by default in JSON-based APIs.).

The endpoint is parametric and `label` can be replaced with any valid string to send data on specialized paths.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Astarte expects a valid timestamp to be attached each time data is produced.
Data is considered delivered when the transport successfully sends the data regardless of the outcome.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 5184000 seconds before it is erased from the database.


## io.edgehog.devicemanager.SystemInfo v0.1

Information about the system

### About

This interface is of type `properties` and is owned by the `device`, meaning that it is the device which initiates the data flow.
Thanks to this type of interface, the device can set a persistent, stateful, synchronized state with no concept of history or timestamping.


### Mappings

The interface has the following mappings:

- `/serialNumber` with `string` type. The serial number of the system
- `/partNumber` with `string` type. The part number of the system


### `/serialNumber`

The serial number of the system



This endpoint accepts values of type `string`: an UTF-8 string, at most 65536 bytes long.

The value of the property cannot be unset.

### `/partNumber`

The part number of the system



This endpoint accepts values of type `string`: an UTF-8 string, at most 65536 bytes long.

The value of the property cannot be unset.


## io.edgehog.devicemanager.SystemStatus v0.1



### About

This interface is of type `datastream` and is owned by the `device`, meaning that it is the device which initiates the data flow.
Thanks to this type of interface, the device can send a mutable, ordered stream of data, with no concept of persistent state or synchronization.

Data gets sent with an `object` aggregation.
Astarte expects the owner to send all of the interface's mappings at the same time, packed in a single message.

### Mappings

The interface has the following mappings:

- `/systemStatus/availMemoryBytes` with `longinteger` type. Available memory (Bytes)
- `/systemStatus/bootId` with `string` type. UUID representing the Boot Id
- `/systemStatus/taskCount` with `integer` type. Number of running tasks or processes
- `/systemStatus/uptimeMillis` with `longinteger` type. Get time in milliseconds since boot


### `/systemStatus/availMemoryBytes`

Available memory (Bytes)



This endpoint accepts values of type `longinteger`: a signed 64 bit integer (please note that longinteger is represented as a string by default in JSON-based APIs.).

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Astarte expects a valid timestamp to be attached each time data is produced.
Data is considered delivered when the transport successfully sends the data regardless of the outcome.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 5184000 seconds before it is erased from the database.

### `/systemStatus/bootId`

UUID representing the Boot Id



This endpoint accepts values of type `string`: an UTF-8 string, at most 65536 bytes long.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Astarte expects a valid timestamp to be attached each time data is produced.
Data is considered delivered when the transport successfully sends the data regardless of the outcome.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 5184000 seconds before it is erased from the database.

### `/systemStatus/taskCount`

Number of running tasks or processes



This endpoint accepts values of type `integer`: a signed 32 bit integer.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Astarte expects a valid timestamp to be attached each time data is produced.
Data is considered delivered when the transport successfully sends the data regardless of the outcome.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 5184000 seconds before it is erased from the database.

### `/systemStatus/uptimeMillis`

Get time in milliseconds since boot



This endpoint accepts values of type `longinteger`: a signed 64 bit integer (please note that longinteger is represented as a string by default in JSON-based APIs.).

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Astarte expects a valid timestamp to be attached each time data is produced.
Data is considered delivered when the transport successfully sends the data regardless of the outcome.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 5184000 seconds before it is erased from the database.


## io.edgehog.devicemanager.WiFiScanResults v0.2



### About

This interface is of type `datastream` and is owned by the `device`, meaning that it is the device which initiates the data flow.
Thanks to this type of interface, the device can send a mutable, ordered stream of data, with no concept of persistent state or synchronization.

Data gets sent with an `object` aggregation.
Astarte expects the owner to send all of the interface's mappings at the same time, packed in a single message.

### Mappings

The interface has the following mappings:

- `/ap/channel` with `integer` type. The channel over which the client is communicating with the access point.
- `/ap/connected` with `boolean` type. Identifies if the device is connected to this Access Point
- `/ap/essid` with `string` type. Extended Service Set Identification of the current AP, empty string if the AP is hidden.
- `/ap/macAddress` with `string` type. Lower case mac address string formatted like `de:ad:be:ff:11:22`.
- `/ap/rssi` with `integer` type. The current signal strength measured in dBm.


### `/ap/channel`

The channel over which the client is communicating with the access point.

The channel represents one of the ranges into which the reference frequency is divided and it's identified by an integer number in the range 1 - 165, depending on the frequency itself and the region.

This endpoint accepts values of type `integer`: a signed 32 bit integer.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Astarte expects a valid timestamp to be attached each time data is produced.
Data is considered delivered when the transport successfully sends the data regardless of the outcome.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 5184000 seconds before it is erased from the database.

### `/ap/connected`

Identifies if the device is connected to this Access Point



This endpoint accepts values of type `boolean`: either true or false, adhering to JSON boolean type.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Astarte expects a valid timestamp to be attached each time data is produced.
Data is considered delivered when the transport successfully sends the data regardless of the outcome.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 5184000 seconds before it is erased from the database.

### `/ap/essid`

Extended Service Set Identification of the current AP, empty string if the AP is hidden.



This endpoint accepts values of type `string`: an UTF-8 string, at most 65536 bytes long.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Astarte expects a valid timestamp to be attached each time data is produced.
Data is considered delivered when the transport successfully sends the data regardless of the outcome.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 5184000 seconds before it is erased from the database.

### `/ap/macAddress`

Lower case mac address string formatted like `de:ad:be:ff:11:22`.



This endpoint accepts values of type `string`: an UTF-8 string, at most 65536 bytes long.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Astarte expects a valid timestamp to be attached each time data is produced.
Data is considered delivered when the transport successfully sends the data regardless of the outcome.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 5184000 seconds before it is erased from the database.

### `/ap/rssi`

The current signal strength measured in dBm.



This endpoint accepts values of type `integer`: a signed 32 bit integer.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Astarte expects a valid timestamp to be attached each time data is produced.
Data is considered delivered when the transport successfully sends the data regardless of the outcome.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 5184000 seconds before it is erased from the database.


## io.edgehog.devicemanager.apps.AvailableContainers v0.1



### About

This interface is of type `properties` and is owned by the `device`, meaning that it is the device which initiates the data flow.
Thanks to this type of interface, the device can set a persistent, stateful, synchronized state with no concept of history or timestamping.


### Mappings

The interface has the following mappings:

- `/%{container_id}/status` with `string` type. Container status


### `/%{container_id}/status`

Container status

Possible values [Received, Created, Running, Stopped]

This endpoint accepts values of type `string`: an UTF-8 string, at most 65536 bytes long.

The endpoint is parametric and `container_id` can be replaced with any valid string to send data on specialized paths.

The value of the property can be unset.


## io.edgehog.devicemanager.apps.AvailableDeployments v0.1



### About

This interface is of type `properties` and is owned by the `device`, meaning that it is the device which initiates the data flow.
Thanks to this type of interface, the device can set a persistent, stateful, synchronized state with no concept of history or timestamping.


### Mappings

The interface has the following mappings:

- `/%{deployment_id}/status` with `string` type. Status of the deployment


### `/%{deployment_id}/status`

Status of the deployment

Possible values: [Stopped, Started]

This endpoint accepts values of type `string`: an UTF-8 string, at most 65536 bytes long.

The endpoint is parametric and `deployment_id` can be replaced with any valid string to send data on specialized paths.

The value of the property can be unset.


## io.edgehog.devicemanager.apps.AvailableDeviceMappings v0.1



### About

This interface is of type `properties` and is owned by the `device`, meaning that it is the device which initiates the data flow.
Thanks to this type of interface, the device can set a persistent, stateful, synchronized state with no concept of history or timestamping.


### Mappings

The interface has the following mappings:

- `/%{device_mapping_id}/present` with `boolean` type. The device is present on the host


### `/%{device_mapping_id}/present`

The device is present on the host



This endpoint accepts values of type `boolean`: either true or false, adhering to JSON boolean type.

The endpoint is parametric and `device_mapping_id` can be replaced with any valid string to send data on specialized paths.

The value of the property can be unset.


## io.edgehog.devicemanager.apps.AvailableImages v0.1

Properties available for a specific Docker image on the device

### About

This interface is of type `properties` and is owned by the `device`, meaning that it is the device which initiates the data flow.
Thanks to this type of interface, the device can set a persistent, stateful, synchronized state with no concept of history or timestamping.


### Mappings

The interface has the following mappings:

- `/%{image_id}/pulled` with `boolean` type. Pulled image


### `/%{image_id}/pulled`

Pulled image



This endpoint accepts values of type `boolean`: either true or false, adhering to JSON boolean type.

The endpoint is parametric and `image_id` can be replaced with any valid string to send data on specialized paths.

The value of the property can be unset.


## io.edgehog.devicemanager.apps.AvailableNetworks v0.1



### About

This interface is of type `properties` and is owned by the `device`, meaning that it is the device which initiates the data flow.
Thanks to this type of interface, the device can set a persistent, stateful, synchronized state with no concept of history or timestamping.


### Mappings

The interface has the following mappings:

- `/%{network_id}/created` with `boolean` type. Network was created


### `/%{network_id}/created`

Network was created



This endpoint accepts values of type `boolean`: either true or false, adhering to JSON boolean type.

The endpoint is parametric and `network_id` can be replaced with any valid string to send data on specialized paths.

The value of the property can be unset.


## io.edgehog.devicemanager.apps.AvailableVolumes v0.1



### About

This interface is of type `properties` and is owned by the `device`, meaning that it is the device which initiates the data flow.
Thanks to this type of interface, the device can set a persistent, stateful, synchronized state with no concept of history or timestamping.


### Mappings

The interface has the following mappings:

- `/%{volume_id}/created` with `boolean` type. Volume created


### `/%{volume_id}/created`

Volume created



This endpoint accepts values of type `boolean`: either true or false, adhering to JSON boolean type.

The endpoint is parametric and `volume_id` can be replaced with any valid string to send data on specialized paths.

The value of the property can be unset.


## io.edgehog.devicemanager.apps.CreateContainerRequest v0.1



### About

This interface is of type `datastream` and is owned by the `server`, meaning that it is the server which initiates the data flow.
Thanks to this type of interface, the server can send a mutable, ordered stream of data, with no concept of persistent state or synchronization.

Data gets sent with an `object` aggregation.
Astarte expects the owner to send all of the interface's mappings at the same time, packed in a single message.

### Mappings

The interface has the following mappings:

- `/container/id` with `string` type. Create Container Request id
- `/container/deploymentId` with `string` type. Reference to a Deployment using the container
- `/container/imageId` with `string` type. Container image id
- `/container/networkIds` with `stringarray` type. Container network ids
- `/container/volumeIds` with `stringarray` type. Container volume ids
- `/container/deviceMappingIds` with `stringarray` type. Container device mappings ids
- `/container/hostname` with `string` type. Container hostname
- `/container/restartPolicy` with `string` type. Container restart policy
- `/container/env` with `stringarray` type. Container environment
- `/container/binds` with `stringarray` type. Container binds
- `/container/networkMode` with `string` type. Network mode used for this container.
- `/container/portBindings` with `stringarray` type. Container port bindings
- `/container/extraHosts` with `stringarray` type. List of hostname/IP to add to the container's /etc/hosts
- `/container/capAdd` with `stringarray` type. A list of kernel capabilities to add to the container.
- `/container/capDrop` with `stringarray` type. A list of kernel capabilities to drop from the container.
- `/container/cpuPeriod` with `longinteger` type. The length of a CPU period in microseconds.
- `/container/cpuQuota` with `longinteger` type. Microseconds of CPU time that the container can get in a CPU period.
- `/container/cpuRealtimePeriod` with `longinteger` type. The length of a CPU real-time period in microseconds.
- `/container/cpuRealtimeRuntime` with `longinteger` type. The length of a CPU real-time runtime in microseconds.
- `/container/memory` with `longinteger` type. Memory limit in bytes.
- `/container/memoryReservation` with `longinteger` type. Memory soft limit in bytes. Default to 0 for unlimited. Unset if the value is -1 (or negative).
- `/container/memorySwap` with `longinteger` type. Total memory limit (memory + swap).
- `/container/memorySwappiness` with `integer` type. Memory swappiness
- `/container/volumeDriver` with `string` type. Driver that this container uses to mount volumes.
- `/container/storageOpt` with `stringarray` type. Storage driver options for this container.
- `/container/readOnlyRootfs` with `boolean` type. Mount the container's root filesystem as read only.
- `/container/tmpfs` with `stringarray` type. A map of container directories which should be replaced by tmpfs mounts.
- `/container/privileged` with `boolean` type. Run privileged


### `/container/id`

Create Container Request id

Unique id for the container.

This endpoint accepts values of type `string`: an UTF-8 string, at most 65536 bytes long.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Data is considered delivered when it has been received at least once by the recipient.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 31556952 seconds before it is erased from the database.

### `/container/deploymentId`

Reference to a Deployment using the container

The deployment in which the container is used, so the device can send deployment events to Astarte for the create request

This endpoint accepts values of type `string`: an UTF-8 string, at most 65536 bytes long.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Data is considered delivered when it has been received at least once by the recipient.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 31556952 seconds before it is erased from the database.

### `/container/imageId`

Container image id

The id of the image to use when creating the container.

This endpoint accepts values of type `string`: an UTF-8 string, at most 65536 bytes long.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Data is considered delivered when it has been received at least once by the recipient.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 31556952 seconds before it is erased from the database.

### `/container/networkIds`

Container network ids

The ids of the network to connect with the container.

This endpoint accepts values of type `stringarray`: a list of values, represented as a JSON Array. Arrays can have up to 1024 items and each item must respect the limits of its scalar type.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Data is considered delivered when it has been received at least once by the recipient.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 31556952 seconds before it is erased from the database.

### `/container/volumeIds`

Container volume ids

The ids of the volumes to mount on the container.

This endpoint accepts values of type `stringarray`: a list of values, represented as a JSON Array. Arrays can have up to 1024 items and each item must respect the limits of its scalar type.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Data is considered delivered when it has been received at least once by the recipient.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 31556952 seconds before it is erased from the database.

### `/container/deviceMappingIds`

Container device mappings ids

The ids of the device mappings to mount on the container.

This endpoint accepts values of type `stringarray`: a list of values, represented as a JSON Array. Arrays can have up to 1024 items and each item must respect the limits of its scalar type.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Data is considered delivered when it has been received at least once by the recipient.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 31556952 seconds before it is erased from the database.

### `/container/hostname`

Container hostname

The hostname to use for the container, as a valid RFC 1123 hostname.

This endpoint accepts values of type `string`: an UTF-8 string, at most 65536 bytes long.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Data is considered delivered when it has been received at least once by the recipient.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 31556952 seconds before it is erased from the database.

### `/container/restartPolicy`

Container restart policy

The behavior to apply when the container exits. Possible values are: ['', 'no', 'always' 'unless-stopped', 'on-failure']

This endpoint accepts values of type `string`: an UTF-8 string, at most 65536 bytes long.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Data is considered delivered when it has been received at least once by the recipient.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 31556952 seconds before it is erased from the database.

### `/container/env`

Container environment

Array of key=value environment variables. The key cannot contain `=`.

This endpoint accepts values of type `stringarray`: a list of values, represented as a JSON Array. Arrays can have up to 1024 items and each item must respect the limits of its scalar type.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Data is considered delivered when it has been received at least once by the recipient.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 31556952 seconds before it is erased from the database.

### `/container/binds`

Container binds

A list of volume bindings for this container. Each volume binding is a string in one of these forms: host-src:container-dest[:options], or volume-name:container-dest[:options]. The container-dest must be an absolute path.

This endpoint accepts values of type `stringarray`: a list of values, represented as a JSON Array. Arrays can have up to 1024 items and each item must respect the limits of its scalar type.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Data is considered delivered when it has been received at least once by the recipient.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 31556952 seconds before it is erased from the database.

### `/container/networkMode`

Network mode used for this container.

Supported standard values are: bridge, host, none, and container:<name|id>. Any other value is taken as a custom network's name to which this container should connect to. If you are using a different container engine than docker, there could be other values.

This endpoint accepts values of type `string`: an UTF-8 string, at most 65536 bytes long.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Data is considered delivered when it has been received at least once by the recipient.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 31556952 seconds before it is erased from the database.

### `/container/portBindings`

Container port bindings

Array of ip:[host_port:]container_port[/protocol] | [hostPort:]containerPort[/protocol]. Protocol is TCP by default

This endpoint accepts values of type `stringarray`: a list of values, represented as a JSON Array. Arrays can have up to 1024 items and each item must respect the limits of its scalar type.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Data is considered delivered when it has been received at least once by the recipient.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 31556952 seconds before it is erased from the database.

### `/container/extraHosts`

List of hostname/IP to add to the container's /etc/hosts

A list of hostnames/IP mappings to add to the container's /etc/hosts file. Specified in the form ["hostname:IP"]. You can use the `host-gateway` to connect to the host IP

This endpoint accepts values of type `stringarray`: a list of values, represented as a JSON Array. Arrays can have up to 1024 items and each item must respect the limits of its scalar type.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Data is considered delivered when it has been received at least once by the recipient.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 31556952 seconds before it is erased from the database.

### `/container/capAdd`

A list of kernel capabilities to add to the container.

A list of kernel capabilities to add to the container.

This endpoint accepts values of type `stringarray`: a list of values, represented as a JSON Array. Arrays can have up to 1024 items and each item must respect the limits of its scalar type.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Data is considered delivered when it has been received at least once by the recipient.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 31556952 seconds before it is erased from the database.

### `/container/capDrop`

A list of kernel capabilities to drop from the container.

A list of kernel capabilities to drop from the container.

This endpoint accepts values of type `stringarray`: a list of values, represented as a JSON Array. Arrays can have up to 1024 items and each item must respect the limits of its scalar type.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Data is considered delivered when it has been received at least once by the recipient.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 31556952 seconds before it is erased from the database.

### `/container/cpuPeriod`

The length of a CPU period in microseconds.

Unset if the value is -1 (or negative) and the cpuQuota must also be unset.

This endpoint accepts values of type `longinteger`: a signed 64 bit integer (please note that longinteger is represented as a string by default in JSON-based APIs.).

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Data is considered delivered when it has been received at least once by the recipient.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 31556952 seconds before it is erased from the database.

### `/container/cpuQuota`

Microseconds of CPU time that the container can get in a CPU period.

Unset if the value is -1 (or negative) and the cpuPeriod must also be unset.

This endpoint accepts values of type `longinteger`: a signed 64 bit integer (please note that longinteger is represented as a string by default in JSON-based APIs.).

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Data is considered delivered when it has been received at least once by the recipient.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 31556952 seconds before it is erased from the database.

### `/container/cpuRealtimePeriod`

The length of a CPU real-time period in microseconds.

The length of a CPU real-time period in microseconds. Set to 0 to allocate no time allocated to real-time tasks. Unset if the value is -1 (or negative).

This endpoint accepts values of type `longinteger`: a signed 64 bit integer (please note that longinteger is represented as a string by default in JSON-based APIs.).

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Data is considered delivered when it has been received at least once by the recipient.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 31556952 seconds before it is erased from the database.

### `/container/cpuRealtimeRuntime`

The length of a CPU real-time runtime in microseconds.

The length of a CPU real-time runtime in microseconds. Set to 0 to allocate no time allocated to real-time tasks. Unset if the value is -1 (or negative).

This endpoint accepts values of type `longinteger`: a signed 64 bit integer (please note that longinteger is represented as a string by default in JSON-based APIs.).

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Data is considered delivered when it has been received at least once by the recipient.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 31556952 seconds before it is erased from the database.

### `/container/memory`

Memory limit in bytes.

Memory limit in bytes. Default to 0 for unlimited. Unset if the value is -1 (or negative).

This endpoint accepts values of type `longinteger`: a signed 64 bit integer (please note that longinteger is represented as a string by default in JSON-based APIs.).

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Data is considered delivered when it has been received at least once by the recipient.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 31556952 seconds before it is erased from the database.

### `/container/memoryReservation`

Memory soft limit in bytes. Default to 0 for unlimited. Unset if the value is -1 (or negative).



This endpoint accepts values of type `longinteger`: a signed 64 bit integer (please note that longinteger is represented as a string by default in JSON-based APIs.).

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Data is considered delivered when it has been received at least once by the recipient.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 31556952 seconds before it is erased from the database.

### `/container/memorySwap`

Total memory limit (memory + swap).

Total memory limit (memory + swap). Set as -1 to enable unlimited swap. Unset if the value is -2 (or more negative).

This endpoint accepts values of type `longinteger`: a signed 64 bit integer (please note that longinteger is represented as a string by default in JSON-based APIs.).

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Data is considered delivered when it has been received at least once by the recipient.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 31556952 seconds before it is erased from the database.

### `/container/memorySwappiness`

Memory swappiness

Tune a container's memory swappiness behavior. Accepts an integer between 0 and 100. Unset if the value is -1 (or negative).

This endpoint accepts values of type `integer`: a signed 32 bit integer.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Data is considered delivered when it has been received at least once by the recipient.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 31556952 seconds before it is erased from the database.

### `/container/volumeDriver`

Driver that this container uses to mount volumes.



This endpoint accepts values of type `string`: an UTF-8 string, at most 65536 bytes long.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Data is considered delivered when it has been received at least once by the recipient.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 31556952 seconds before it is erased from the database.

### `/container/storageOpt`

Storage driver options for this container.

Storage driver options for this container, in the form "size=120G".

This endpoint accepts values of type `stringarray`: a list of values, represented as a JSON Array. Arrays can have up to 1024 items and each item must respect the limits of its scalar type.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Data is considered delivered when it has been received at least once by the recipient.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 31556952 seconds before it is erased from the database.

### `/container/readOnlyRootfs`

Mount the container's root filesystem as read only.



This endpoint accepts values of type `boolean`: either true or false, adhering to JSON boolean type.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Data is considered delivered when it has been received at least once by the recipient.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 31556952 seconds before it is erased from the database.

### `/container/tmpfs`

A map of container directories which should be replaced by tmpfs mounts.

A map of container directories which should be replaced by tmpfs mounts, and their corresponding mount options. For example:
 "/run=rw,noexec,nosuid,size=65536k"

This endpoint accepts values of type `stringarray`: a list of values, represented as a JSON Array. Arrays can have up to 1024 items and each item must respect the limits of its scalar type.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Data is considered delivered when it has been received at least once by the recipient.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 31556952 seconds before it is erased from the database.

### `/container/privileged`

Run privileged

Runs the exec process with extended privileges.

This endpoint accepts values of type `boolean`: either true or false, adhering to JSON boolean type.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Data is considered delivered when it has been received at least once by the recipient.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 31556952 seconds before it is erased from the database.


## io.edgehog.devicemanager.apps.CreateDeploymentRequest v0.1



### About

This interface is of type `datastream` and is owned by the `server`, meaning that it is the server which initiates the data flow.
Thanks to this type of interface, the server can send a mutable, ordered stream of data, with no concept of persistent state or synchronization.

Data gets sent with an `object` aggregation.
Astarte expects the owner to send all of the interface's mappings at the same time, packed in a single message.

### Mappings

The interface has the following mappings:

- `/deployment/id` with `string` type. Create Deployment Request id
- `/deployment/containers` with `stringarray` type. Deployment containers


### `/deployment/id`

Create Deployment Request id

Unique id for the deployment.

This endpoint accepts values of type `string`: an UTF-8 string, at most 65536 bytes long.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Data is considered delivered when it has been received at least once by the recipient.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 31556952 seconds before it is erased from the database.

### `/deployment/containers`

Deployment containers

Containers used by the deployment.

This endpoint accepts values of type `stringarray`: a list of values, represented as a JSON Array. Arrays can have up to 1024 items and each item must respect the limits of its scalar type.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Data is considered delivered when it has been received at least once by the recipient.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 31556952 seconds before it is erased from the database.


## io.edgehog.devicemanager.apps.CreateDeviceMappingRequest v0.1



### About

This interface is of type `datastream` and is owned by the `server`, meaning that it is the server which initiates the data flow.
Thanks to this type of interface, the server can send a mutable, ordered stream of data, with no concept of persistent state or synchronization.

Data gets sent with an `object` aggregation.
Astarte expects the owner to send all of the interface's mappings at the same time, packed in a single message.

### Mappings

The interface has the following mappings:

- `/deviceMapping/id` with `string` type. Create Device Mapping Request id
- `/deviceMapping/deploymentId` with `string` type. Reference to a Deployment using the device mapping
- `/deviceMapping/pathOnHost` with `string` type. Path on host for the device
- `/deviceMapping/pathInContainer` with `string` type. Path in the container for the device
- `/deviceMapping/cGroupPermissions` with `string` type. Permissions on the device.


### `/deviceMapping/id`

Create Device Mapping Request id

Unique id for the container.

This endpoint accepts values of type `string`: an UTF-8 string, at most 65536 bytes long.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Data is considered delivered when it has been received at least once by the recipient.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 31556952 seconds before it is erased from the database.

### `/deviceMapping/deploymentId`

Reference to a Deployment using the device mapping

The deployment in which the device mapping is used, so the device can send deployment events to Astarte for the create request

This endpoint accepts values of type `string`: an UTF-8 string, at most 65536 bytes long.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Data is considered delivered when it has been received at least once by the recipient.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 31556952 seconds before it is erased from the database.

### `/deviceMapping/pathOnHost`

Path on host for the device

Path on host for the device, for example '/dev/deviceName'

This endpoint accepts values of type `string`: an UTF-8 string, at most 65536 bytes long.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Data is considered delivered when it has been received at least once by the recipient.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 31556952 seconds before it is erased from the database.

### `/deviceMapping/pathInContainer`

Path in the container for the device

Path in the container for the device, for example '/dev/deviceName'

This endpoint accepts values of type `string`: an UTF-8 string, at most 65536 bytes long.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Data is considered delivered when it has been received at least once by the recipient.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 31556952 seconds before it is erased from the database.

### `/deviceMapping/cGroupPermissions`

Permissions on the device.

Permissions on the device, for example 'mrw'

This endpoint accepts values of type `string`: an UTF-8 string, at most 65536 bytes long.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Data is considered delivered when it has been received at least once by the recipient.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 31556952 seconds before it is erased from the database.


## io.edgehog.devicemanager.apps.CreateImageRequest v0.1

Request to pull and create a container image.

The ttl of this datastream is short to keep the sensitive fields private.

### About

This interface is of type `datastream` and is owned by the `server`, meaning that it is the server which initiates the data flow.
Thanks to this type of interface, the server can send a mutable, ordered stream of data, with no concept of persistent state or synchronization.

Data gets sent with an `object` aggregation.
Astarte expects the owner to send all of the interface's mappings at the same time, packed in a single message.

### Mappings

The interface has the following mappings:

- `/image/id` with `string` type. Create Image Request id
- `/image/deploymentId` with `string` type. Reference to a Deployment using the image
- `/image/reference` with `string` type. Image reference to be pulled
- `/image/registryAuth` with `string` type. Image registry authentication header


### `/image/id`

Create Image Request id

Unique id for the container image.

This endpoint accepts values of type `string`: an UTF-8 string, at most 65536 bytes long.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Data is considered delivered when it has been received at least once by the recipient.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 600 seconds before it is erased from the database.

### `/image/deploymentId`

Reference to a Deployment using the image

The deployment in which the image is used, so the device can send deployment events to Astarte for the create request

This endpoint accepts values of type `string`: an UTF-8 string, at most 65536 bytes long.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Data is considered delivered when it has been received at least once by the recipient.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 600 seconds before it is erased from the database.

### `/image/reference`

Image reference to be pulled

Name of the image to pull. It should be in the form [regitry-host[:port]/][image-repo/]image-name[:(tag|digest)]

This endpoint accepts values of type `string`: an UTF-8 string, at most 65536 bytes long.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Data is considered delivered when it has been received at least once by the recipient.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 600 seconds before it is erased from the database.

### `/image/registryAuth`

Image registry authentication header

Optional base64url-encoded JSON for the auth configuration to the registry. An empty string means the image is public and doesn't require authentication. See https://docs.docker.com/reference/api/engine/version/v1.43/#section/Authentication for more information.

This endpoint accepts values of type `string`: an UTF-8 string, at most 65536 bytes long.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Data is considered delivered when it has been received at least once by the recipient.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 600 seconds before it is erased from the database.


## io.edgehog.devicemanager.apps.CreateNetworkRequest v0.1



### About

This interface is of type `datastream` and is owned by the `server`, meaning that it is the server which initiates the data flow.
Thanks to this type of interface, the server can send a mutable, ordered stream of data, with no concept of persistent state or synchronization.

Data gets sent with an `object` aggregation.
Astarte expects the owner to send all of the interface's mappings at the same time, packed in a single message.

### Mappings

The interface has the following mappings:

- `/network/id` with `string` type. Create Network Request id
- `/network/deploymentId` with `string` type. Reference to a Deployment using the network
- `/network/driver` with `string` type. Network driver
- `/network/internal` with `boolean` type. Internal network
- `/network/enableIpv6` with `boolean` type. Enable IPv6
- `/network/options` with `stringarray` type. Network driver options


### `/network/id`

Create Network Request id

Unique id for the container network.

This endpoint accepts values of type `string`: an UTF-8 string, at most 65536 bytes long.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Data is considered delivered when it has been received at least once by the recipient.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 31556952 seconds before it is erased from the database.

### `/network/deploymentId`

Reference to a Deployment using the network

The deployment in which the network is used, so the device can send deployment events to Astarte for the create request

This endpoint accepts values of type `string`: an UTF-8 string, at most 65536 bytes long.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Data is considered delivered when it has been received at least once by the recipient.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 31556952 seconds before it is erased from the database.

### `/network/driver`

Network driver

Name of the network driver plugin to use.

This endpoint accepts values of type `string`: an UTF-8 string, at most 65536 bytes long.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Data is considered delivered when it has been received at least once by the recipient.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 31556952 seconds before it is erased from the database.

### `/network/internal`

Internal network

Restrict external access to the network.

This endpoint accepts values of type `boolean`: either true or false, adhering to JSON boolean type.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Data is considered delivered when it has been received at least once by the recipient.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 31556952 seconds before it is erased from the database.

### `/network/enableIpv6`

Enable IPv6

Enable IPv6 on the network.

This endpoint accepts values of type `boolean`: either true or false, adhering to JSON boolean type.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Data is considered delivered when it has been received at least once by the recipient.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 31556952 seconds before it is erased from the database.

### `/network/options`

Network driver options

An array of key=value options to set for the driver. The key cannot contain an `=`.

This endpoint accepts values of type `stringarray`: a list of values, represented as a JSON Array. Arrays can have up to 1024 items and each item must respect the limits of its scalar type.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Data is considered delivered when it has been received at least once by the recipient.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 31556952 seconds before it is erased from the database.


## io.edgehog.devicemanager.apps.CreateVolumeRequest v0.1



### About

This interface is of type `datastream` and is owned by the `server`, meaning that it is the server which initiates the data flow.
Thanks to this type of interface, the server can send a mutable, ordered stream of data, with no concept of persistent state or synchronization.

Data gets sent with an `object` aggregation.
Astarte expects the owner to send all of the interface's mappings at the same time, packed in a single message.

### Mappings

The interface has the following mappings:

- `/volume/id` with `string` type. Create Volume Request id
- `/volume/deploymentId` with `string` type. Reference to a Deployment using the volume
- `/volume/driver` with `string` type. Volume driver name
- `/volume/options` with `stringarray` type. Volume driver options


### `/volume/id`

Create Volume Request id

Unique id for the volume.

This endpoint accepts values of type `string`: an UTF-8 string, at most 65536 bytes long.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Data is considered delivered when it has been received at least once by the recipient.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 31556952 seconds before it is erased from the database.

### `/volume/deploymentId`

Reference to a Deployment using the volume

The deployment in which the volume is used, so the device can send deployment events to Astarte for the create request

This endpoint accepts values of type `string`: an UTF-8 string, at most 65536 bytes long.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Data is considered delivered when it has been received at least once by the recipient.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 31556952 seconds before it is erased from the database.

### `/volume/driver`

Volume driver name

Name of the volume driver to use.

This endpoint accepts values of type `string`: an UTF-8 string, at most 65536 bytes long.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Data is considered delivered when it has been received at least once by the recipient.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 31556952 seconds before it is erased from the database.

### `/volume/options`

Volume driver options

An array of key=value options to set for the driver. The key cannot contain an `=`.

This endpoint accepts values of type `stringarray`: a list of values, represented as a JSON Array. Arrays can have up to 1024 items and each item must respect the limits of its scalar type.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Data is considered delivered when it has been received at least once by the recipient.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 31556952 seconds before it is erased from the database.


## io.edgehog.devicemanager.apps.DeploymentCommand v0.1



### About

This interface is of type `datastream` and is owned by the `server`, meaning that it is the server which initiates the data flow.
Thanks to this type of interface, the server can send a mutable, ordered stream of data, with no concept of persistent state or synchronization.

Data gets sent with an `individual` aggregation.
Each mapping is treated as an independent value and is managed individually.

### Mappings

The interface has the following mappings:

- `/%{deployment_id}/command` with `string` type. Deployment command


### `/%{deployment_id}/command`

Deployment command

Possible values [Start, Stop, Delete]

This endpoint accepts values of type `string`: an UTF-8 string, at most 65536 bytes long.

The endpoint is parametric and `deployment_id` can be replaced with any valid string to send data on specialized paths.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Data is considered delivered when the transport successfully sends the data regardless of the outcome.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 31556952 seconds before it is erased from the database.


## io.edgehog.devicemanager.apps.DeploymentEvent v0.2



### About

This interface is of type `datastream` and is owned by the `device`, meaning that it is the device which initiates the data flow.
Thanks to this type of interface, the device can send a mutable, ordered stream of data, with no concept of persistent state or synchronization.

Data gets sent with an `object` aggregation.
Astarte expects the owner to send all of the interface's mappings at the same time, packed in a single message.

### Mappings

The interface has the following mappings:

- `/%{deployment_id}/status` with `string` type. Deployment status
- `/%{deployment_id}/message` with `string` type. Optional message for the event
- `/%{deployment_id}/addInfo` with `stringarray` type. Additional info


### `/%{deployment_id}/status`

Deployment status

Possible values: [Starting, Started, Stopping, Stopped, Updating, Deleting, Error]

This endpoint accepts values of type `string`: an UTF-8 string, at most 65536 bytes long.

The endpoint is parametric and `deployment_id` can be replaced with any valid string to send data on specialized paths.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Astarte expects a valid timestamp to be attached each time data is produced.
Data is considered delivered when the transport successfully sends the data regardless of the outcome.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 31556952 seconds before it is erased from the database.

### `/%{deployment_id}/message`

Optional message for the event



This endpoint accepts values of type `string`: an UTF-8 string, at most 65536 bytes long.

The endpoint is parametric and `deployment_id` can be replaced with any valid string to send data on specialized paths.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Astarte expects a valid timestamp to be attached each time data is produced.
Data is considered delivered when the transport successfully sends the data regardless of the outcome.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 31556952 seconds before it is erased from the database.

### `/%{deployment_id}/addInfo`

Additional info

Additional info about the event.

This endpoint accepts values of type `stringarray`: a list of values, represented as a JSON Array. Arrays can have up to 1024 items and each item must respect the limits of its scalar type.

The endpoint is parametric and `deployment_id` can be replaced with any valid string to send data on specialized paths.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Astarte expects a valid timestamp to be attached each time data is produced.
Data is considered delivered when the transport successfully sends the data regardless of the outcome.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 31556952 seconds before it is erased from the database.


## io.edgehog.devicemanager.apps.DeploymentUpdate v0.1



### About

This interface is of type `datastream` and is owned by the `server`, meaning that it is the server which initiates the data flow.
Thanks to this type of interface, the server can send a mutable, ordered stream of data, with no concept of persistent state or synchronization.

Data gets sent with an `object` aggregation.
Astarte expects the owner to send all of the interface's mappings at the same time, packed in a single message.

### Mappings

The interface has the following mappings:

- `/deployment/from` with `string` type. Id of the deployment to update from
- `/deployment/to` with `string` type. Id of the deployment to update to


### `/deployment/from`

Id of the deployment to update from



This endpoint accepts values of type `string`: an UTF-8 string, at most 65536 bytes long.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Data is considered delivered when the transport successfully sends the data regardless of the outcome.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 31556952 seconds before it is erased from the database.

### `/deployment/to`

Id of the deployment to update to



This endpoint accepts values of type `string`: an UTF-8 string, at most 65536 bytes long.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Data is considered delivered when the transport successfully sends the data regardless of the outcome.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 31556952 seconds before it is erased from the database.


## io.edgehog.devicemanager.apps.stats.ContainerBlkio v0.1

BlkioStats stores all IO service stats for data read and write.

### About

This interface is of type `datastream` and is owned by the `device`, meaning that it is the device which initiates the data flow.
Thanks to this type of interface, the device can send a mutable, ordered stream of data, with no concept of persistent state or synchronization.

Data gets sent with an `object` aggregation.
Astarte expects the owner to send all of the interface's mappings at the same time, packed in a single message.

### Mappings

The interface has the following mappings:

- `/%{container_id}/name` with `string` type. 
- `/%{container_id}/major` with `longinteger` type. 
- `/%{container_id}/minor` with `longinteger` type. 
- `/%{container_id}/op` with `string` type. 
- `/%{container_id}/value` with `longinteger` type. 


### `/%{container_id}/name`





This endpoint accepts values of type `string`: an UTF-8 string, at most 65536 bytes long.

The endpoint is parametric and `container_id` can be replaced with any valid string to send data on specialized paths.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Astarte expects a valid timestamp to be attached each time data is produced.
Data is considered delivered when the transport successfully sends the data regardless of the outcome.
Data is discarded if the transport is temporarily uncapable of delivering it.

### `/%{container_id}/major`





This endpoint accepts values of type `longinteger`: a signed 64 bit integer (please note that longinteger is represented as a string by default in JSON-based APIs.).

The endpoint is parametric and `container_id` can be replaced with any valid string to send data on specialized paths.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Astarte expects a valid timestamp to be attached each time data is produced.
Data is considered delivered when the transport successfully sends the data regardless of the outcome.
Data is discarded if the transport is temporarily uncapable of delivering it.

### `/%{container_id}/minor`





This endpoint accepts values of type `longinteger`: a signed 64 bit integer (please note that longinteger is represented as a string by default in JSON-based APIs.).

The endpoint is parametric and `container_id` can be replaced with any valid string to send data on specialized paths.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Astarte expects a valid timestamp to be attached each time data is produced.
Data is considered delivered when the transport successfully sends the data regardless of the outcome.
Data is discarded if the transport is temporarily uncapable of delivering it.

### `/%{container_id}/op`





This endpoint accepts values of type `string`: an UTF-8 string, at most 65536 bytes long.

The endpoint is parametric and `container_id` can be replaced with any valid string to send data on specialized paths.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Astarte expects a valid timestamp to be attached each time data is produced.
Data is considered delivered when the transport successfully sends the data regardless of the outcome.
Data is discarded if the transport is temporarily uncapable of delivering it.

### `/%{container_id}/value`





This endpoint accepts values of type `longinteger`: a signed 64 bit integer (please note that longinteger is represented as a string by default in JSON-based APIs.).

The endpoint is parametric and `container_id` can be replaced with any valid string to send data on specialized paths.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Astarte expects a valid timestamp to be attached each time data is produced.
Data is considered delivered when the transport successfully sends the data regardless of the outcome.
Data is discarded if the transport is temporarily uncapable of delivering it.


## io.edgehog.devicemanager.apps.stats.ContainerCpu v0.1

The precpu stats is the CPU statistic of the previous read, and is used to calculate the CPU usage percentage. It is not an exact copy of the cpu_stats field.

### About

This interface is of type `datastream` and is owned by the `device`, meaning that it is the device which initiates the data flow.
Thanks to this type of interface, the device can send a mutable, ordered stream of data, with no concept of persistent state or synchronization.

Data gets sent with an `object` aggregation.
Astarte expects the owner to send all of the interface's mappings at the same time, packed in a single message.

### Mappings

The interface has the following mappings:

- `/%{container_id}/cpuUsageTotalUsage` with `longinteger` type. Total CPU time consumed in nanoseconds
- `/%{container_id}/cpuUsagePercpuUsage` with `longintegerarray` type. Total CPU time (in nanoseconds) consumed per core
- `/%{container_id}/cpuUsageUsageInKernelmode` with `longinteger` type. Time (in nanoseconds) spent by tasks of the cgroup in kernel mode
- `/%{container_id}/cpuUsageUsageInUsermode` with `longinteger` type. Time (in nanoseconds) spent by tasks of the cgroup in user mode
- `/%{container_id}/systemCpuUsage` with `longinteger` type. System Usage.
- `/%{container_id}/onlineCpus` with `integer` type. Number of online CPUs.
- `/%{container_id}/throttlingDataPeriods` with `longinteger` type. Number of periods with throttling active.
- `/%{container_id}/throttlingDataThrottledPeriods` with `longinteger` type. Number of periods when the container hit its throttling limit.
- `/%{container_id}/throttlingDataThrottledTime` with `longinteger` type. Aggregated time (in nanoseconds) the container was throttled for.
- `/%{container_id}/preCpuUsageTotalUsage` with `longinteger` type. Total CPU time consumed in nanoseconds
- `/%{container_id}/preCpuUsagePercpuUsage` with `longintegerarray` type. Total CPU time (in nanoseconds) consumed per core
- `/%{container_id}/preCpuUsageUsageInKernelmode` with `longinteger` type. Time (in nanoseconds) spent by tasks of the cgroup in kernel mode
- `/%{container_id}/preCpuUsageUsageInUsermode` with `longinteger` type. Time (in nanoseconds) spent by tasks of the cgroup in user mode
- `/%{container_id}/preSystemCpuUsage` with `longinteger` type. System Usage.
- `/%{container_id}/preOnlineCpus` with `integer` type. Number of online CPUs.
- `/%{container_id}/preThrottlingDataPeriods` with `longinteger` type. Number of periods with throttling active.
- `/%{container_id}/preThrottlingDataThrottledPeriods` with `longinteger` type. Number of periods when the container hit its throttling limit.
- `/%{container_id}/preThrottlingDataThrottledTime` with `longinteger` type. Aggregated time (in nanoseconds) the container was throttled for.


### `/%{container_id}/cpuUsageTotalUsage`

Total CPU time consumed in nanoseconds

Total CPU time consumed by the container, in nanoseconds.

This endpoint accepts values of type `longinteger`: a signed 64 bit integer (please note that longinteger is represented as a string by default in JSON-based APIs.).

The endpoint is parametric and `container_id` can be replaced with any valid string to send data on specialized paths.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Astarte expects a valid timestamp to be attached each time data is produced.
Data is considered delivered when the transport successfully sends the data regardless of the outcome.
Data is discarded if the transport is temporarily uncapable of delivering it.

### `/%{container_id}/cpuUsagePercpuUsage`

Total CPU time (in nanoseconds) consumed per core

This field is Linux-specific when using cgroups v1.

This endpoint accepts values of type `longintegerarray`: a list of values, represented as a JSON Array. Arrays can have up to 1024 items and each item must respect the limits of its scalar type.

The endpoint is parametric and `container_id` can be replaced with any valid string to send data on specialized paths.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Astarte expects a valid timestamp to be attached each time data is produced.
Data is considered delivered when the transport successfully sends the data regardless of the outcome.
Data is discarded if the transport is temporarily uncapable of delivering it.

### `/%{container_id}/cpuUsageUsageInKernelmode`

Time (in nanoseconds) spent by tasks of the cgroup in kernel mode

CPU time spent in kernel mode by the container's tasks, in nanoseconds.

This endpoint accepts values of type `longinteger`: a signed 64 bit integer (please note that longinteger is represented as a string by default in JSON-based APIs.).

The endpoint is parametric and `container_id` can be replaced with any valid string to send data on specialized paths.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Astarte expects a valid timestamp to be attached each time data is produced.
Data is considered delivered when the transport successfully sends the data regardless of the outcome.
Data is discarded if the transport is temporarily uncapable of delivering it.

### `/%{container_id}/cpuUsageUsageInUsermode`

Time (in nanoseconds) spent by tasks of the cgroup in user mode



This endpoint accepts values of type `longinteger`: a signed 64 bit integer (please note that longinteger is represented as a string by default in JSON-based APIs.).

The endpoint is parametric and `container_id` can be replaced with any valid string to send data on specialized paths.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Astarte expects a valid timestamp to be attached each time data is produced.
Data is considered delivered when the transport successfully sends the data regardless of the outcome.
Data is discarded if the transport is temporarily uncapable of delivering it.

### `/%{container_id}/systemCpuUsage`

System Usage.



This endpoint accepts values of type `longinteger`: a signed 64 bit integer (please note that longinteger is represented as a string by default in JSON-based APIs.).

The endpoint is parametric and `container_id` can be replaced with any valid string to send data on specialized paths.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Astarte expects a valid timestamp to be attached each time data is produced.
Data is considered delivered when the transport successfully sends the data regardless of the outcome.
Data is discarded if the transport is temporarily uncapable of delivering it.

### `/%{container_id}/onlineCpus`

Number of online CPUs.



This endpoint accepts values of type `integer`: a signed 32 bit integer.

The endpoint is parametric and `container_id` can be replaced with any valid string to send data on specialized paths.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Astarte expects a valid timestamp to be attached each time data is produced.
Data is considered delivered when the transport successfully sends the data regardless of the outcome.
Data is discarded if the transport is temporarily uncapable of delivering it.

### `/%{container_id}/throttlingDataPeriods`

Number of periods with throttling active.



This endpoint accepts values of type `longinteger`: a signed 64 bit integer (please note that longinteger is represented as a string by default in JSON-based APIs.).

The endpoint is parametric and `container_id` can be replaced with any valid string to send data on specialized paths.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Astarte expects a valid timestamp to be attached each time data is produced.
Data is considered delivered when the transport successfully sends the data regardless of the outcome.
Data is discarded if the transport is temporarily uncapable of delivering it.

### `/%{container_id}/throttlingDataThrottledPeriods`

Number of periods when the container hit its throttling limit.



This endpoint accepts values of type `longinteger`: a signed 64 bit integer (please note that longinteger is represented as a string by default in JSON-based APIs.).

The endpoint is parametric and `container_id` can be replaced with any valid string to send data on specialized paths.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Astarte expects a valid timestamp to be attached each time data is produced.
Data is considered delivered when the transport successfully sends the data regardless of the outcome.
Data is discarded if the transport is temporarily uncapable of delivering it.

### `/%{container_id}/throttlingDataThrottledTime`

Aggregated time (in nanoseconds) the container was throttled for.



This endpoint accepts values of type `longinteger`: a signed 64 bit integer (please note that longinteger is represented as a string by default in JSON-based APIs.).

The endpoint is parametric and `container_id` can be replaced with any valid string to send data on specialized paths.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Astarte expects a valid timestamp to be attached each time data is produced.
Data is considered delivered when the transport successfully sends the data regardless of the outcome.
Data is discarded if the transport is temporarily uncapable of delivering it.

### `/%{container_id}/preCpuUsageTotalUsage`

Total CPU time consumed in nanoseconds

Total CPU time consumed by the container, in nanoseconds.

This endpoint accepts values of type `longinteger`: a signed 64 bit integer (please note that longinteger is represented as a string by default in JSON-based APIs.).

The endpoint is parametric and `container_id` can be replaced with any valid string to send data on specialized paths.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Astarte expects a valid timestamp to be attached each time data is produced.
Data is considered delivered when the transport successfully sends the data regardless of the outcome.
Data is discarded if the transport is temporarily uncapable of delivering it.

### `/%{container_id}/preCpuUsagePercpuUsage`

Total CPU time (in nanoseconds) consumed per core

This field is Linux-specific when using cgroups v1.

This endpoint accepts values of type `longintegerarray`: a list of values, represented as a JSON Array. Arrays can have up to 1024 items and each item must respect the limits of its scalar type.

The endpoint is parametric and `container_id` can be replaced with any valid string to send data on specialized paths.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Astarte expects a valid timestamp to be attached each time data is produced.
Data is considered delivered when the transport successfully sends the data regardless of the outcome.
Data is discarded if the transport is temporarily uncapable of delivering it.

### `/%{container_id}/preCpuUsageUsageInKernelmode`

Time (in nanoseconds) spent by tasks of the cgroup in kernel mode

CPU time spent in kernel mode by the container's tasks, in nanoseconds.

This endpoint accepts values of type `longinteger`: a signed 64 bit integer (please note that longinteger is represented as a string by default in JSON-based APIs.).

The endpoint is parametric and `container_id` can be replaced with any valid string to send data on specialized paths.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Astarte expects a valid timestamp to be attached each time data is produced.
Data is considered delivered when the transport successfully sends the data regardless of the outcome.
Data is discarded if the transport is temporarily uncapable of delivering it.

### `/%{container_id}/preCpuUsageUsageInUsermode`

Time (in nanoseconds) spent by tasks of the cgroup in user mode



This endpoint accepts values of type `longinteger`: a signed 64 bit integer (please note that longinteger is represented as a string by default in JSON-based APIs.).

The endpoint is parametric and `container_id` can be replaced with any valid string to send data on specialized paths.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Astarte expects a valid timestamp to be attached each time data is produced.
Data is considered delivered when the transport successfully sends the data regardless of the outcome.
Data is discarded if the transport is temporarily uncapable of delivering it.

### `/%{container_id}/preSystemCpuUsage`

System Usage.



This endpoint accepts values of type `longinteger`: a signed 64 bit integer (please note that longinteger is represented as a string by default in JSON-based APIs.).

The endpoint is parametric and `container_id` can be replaced with any valid string to send data on specialized paths.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Astarte expects a valid timestamp to be attached each time data is produced.
Data is considered delivered when the transport successfully sends the data regardless of the outcome.
Data is discarded if the transport is temporarily uncapable of delivering it.

### `/%{container_id}/preOnlineCpus`

Number of online CPUs.



This endpoint accepts values of type `integer`: a signed 32 bit integer.

The endpoint is parametric and `container_id` can be replaced with any valid string to send data on specialized paths.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Astarte expects a valid timestamp to be attached each time data is produced.
Data is considered delivered when the transport successfully sends the data regardless of the outcome.
Data is discarded if the transport is temporarily uncapable of delivering it.

### `/%{container_id}/preThrottlingDataPeriods`

Number of periods with throttling active.



This endpoint accepts values of type `longinteger`: a signed 64 bit integer (please note that longinteger is represented as a string by default in JSON-based APIs.).

The endpoint is parametric and `container_id` can be replaced with any valid string to send data on specialized paths.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Astarte expects a valid timestamp to be attached each time data is produced.
Data is considered delivered when the transport successfully sends the data regardless of the outcome.
Data is discarded if the transport is temporarily uncapable of delivering it.

### `/%{container_id}/preThrottlingDataThrottledPeriods`

Number of periods when the container hit its throttling limit.



This endpoint accepts values of type `longinteger`: a signed 64 bit integer (please note that longinteger is represented as a string by default in JSON-based APIs.).

The endpoint is parametric and `container_id` can be replaced with any valid string to send data on specialized paths.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Astarte expects a valid timestamp to be attached each time data is produced.
Data is considered delivered when the transport successfully sends the data regardless of the outcome.
Data is discarded if the transport is temporarily uncapable of delivering it.

### `/%{container_id}/preThrottlingDataThrottledTime`

Aggregated time (in nanoseconds) the container was throttled for.



This endpoint accepts values of type `longinteger`: a signed 64 bit integer (please note that longinteger is represented as a string by default in JSON-based APIs.).

The endpoint is parametric and `container_id` can be replaced with any valid string to send data on specialized paths.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Astarte expects a valid timestamp to be attached each time data is produced.
Data is considered delivered when the transport successfully sends the data regardless of the outcome.
Data is discarded if the transport is temporarily uncapable of delivering it.


## io.edgehog.devicemanager.apps.stats.ContainerMemory v0.1



### About

This interface is of type `datastream` and is owned by the `device`, meaning that it is the device which initiates the data flow.
Thanks to this type of interface, the device can send a mutable, ordered stream of data, with no concept of persistent state or synchronization.

Data gets sent with an `object` aggregation.
Astarte expects the owner to send all of the interface's mappings at the same time, packed in a single message.

### Mappings

The interface has the following mappings:

- `/%{container_id}/usage` with `longinteger` type. Current res_counter usage for memory.
- `/%{container_id}/maxUsage` with `longinteger` type. Maximum usage ever recorded.
- `/%{container_id}/failcnt` with `longinteger` type. Number of times memory usage hits limits.
- `/%{container_id}/limit` with `longinteger` type. Memory usage limit


### `/%{container_id}/usage`

Current res_counter usage for memory.

Current total memory usage (RAM + swap) of the container, in bytes.

This endpoint accepts values of type `longinteger`: a signed 64 bit integer (please note that longinteger is represented as a string by default in JSON-based APIs.).

The endpoint is parametric and `container_id` can be replaced with any valid string to send data on specialized paths.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Astarte expects a valid timestamp to be attached each time data is produced.
Data is considered delivered when the transport successfully sends the data regardless of the outcome.
Data is discarded if the transport is temporarily uncapable of delivering it.

### `/%{container_id}/maxUsage`

Maximum usage ever recorded.

The maximum memory usage recorded since the container's start, in bytes.

This endpoint accepts values of type `longinteger`: a signed 64 bit integer (please note that longinteger is represented as a string by default in JSON-based APIs.).

The endpoint is parametric and `container_id` can be replaced with any valid string to send data on specialized paths.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Astarte expects a valid timestamp to be attached each time data is produced.
Data is considered delivered when the transport successfully sends the data regardless of the outcome.
Data is discarded if the transport is temporarily uncapable of delivering it.

### `/%{container_id}/failcnt`

Number of times memory usage hits limits.

The number of times the memory limit has been reached.

This endpoint accepts values of type `longinteger`: a signed 64 bit integer (please note that longinteger is represented as a string by default in JSON-based APIs.).

The endpoint is parametric and `container_id` can be replaced with any valid string to send data on specialized paths.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Astarte expects a valid timestamp to be attached each time data is produced.
Data is considered delivered when the transport successfully sends the data regardless of the outcome.
Data is discarded if the transport is temporarily uncapable of delivering it.

### `/%{container_id}/limit`

Memory usage limit

The memory usage limit for the container

This endpoint accepts values of type `longinteger`: a signed 64 bit integer (please note that longinteger is represented as a string by default in JSON-based APIs.).

The endpoint is parametric and `container_id` can be replaced with any valid string to send data on specialized paths.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Astarte expects a valid timestamp to be attached each time data is produced.
Data is considered delivered when the transport successfully sends the data regardless of the outcome.
Data is discarded if the transport is temporarily uncapable of delivering it.


## io.edgehog.devicemanager.apps.stats.ContainerMemoryStats v0.1

All the stats exported via memory.stat. when using cgroups v2.

### About

This interface is of type `datastream` and is owned by the `device`, meaning that it is the device which initiates the data flow.
Thanks to this type of interface, the device can send a mutable, ordered stream of data, with no concept of persistent state or synchronization.

Data gets sent with an `object` aggregation.
Astarte expects the owner to send all of the interface's mappings at the same time, packed in a single message.

### Mappings

The interface has the following mappings:

- `/%{container_id}/name` with `string` type. Name of the stat
- `/%{container_id}/value` with `longinteger` type. Value of the stat


### `/%{container_id}/name`

Name of the stat



This endpoint accepts values of type `string`: an UTF-8 string, at most 65536 bytes long.

The endpoint is parametric and `container_id` can be replaced with any valid string to send data on specialized paths.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Astarte expects a valid timestamp to be attached each time data is produced.
Data is considered delivered when the transport successfully sends the data regardless of the outcome.
Data is discarded if the transport is temporarily uncapable of delivering it.

### `/%{container_id}/value`

Value of the stat



This endpoint accepts values of type `longinteger`: a signed 64 bit integer (please note that longinteger is represented as a string by default in JSON-based APIs.).

The endpoint is parametric and `container_id` can be replaced with any valid string to send data on specialized paths.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Astarte expects a valid timestamp to be attached each time data is produced.
Data is considered delivered when the transport successfully sends the data regardless of the outcome.
Data is discarded if the transport is temporarily uncapable of delivering it.


## io.edgehog.devicemanager.apps.stats.ContainerNetworks v0.1

Network statistics for the container per interface.

### About

This interface is of type `datastream` and is owned by the `device`, meaning that it is the device which initiates the data flow.
Thanks to this type of interface, the device can send a mutable, ordered stream of data, with no concept of persistent state or synchronization.

Data gets sent with an `object` aggregation.
Astarte expects the owner to send all of the interface's mappings at the same time, packed in a single message.

### Mappings

The interface has the following mappings:

- `/%{container_id}/interface` with `string` type. Network interface name
- `/%{container_id}/rxBytes` with `longinteger` type. Bytes received.
- `/%{container_id}/rxPackets` with `longinteger` type. Packets received.
- `/%{container_id}/rxDropped` with `longinteger` type. Incoming packets dropped.
- `/%{container_id}/rxErrors` with `longinteger` type. Received errors.
- `/%{container_id}/txBytes` with `longinteger` type. Bytes sent.
- `/%{container_id}/txPackets` with `longinteger` type. Packets sent.
- `/%{container_id}/txErrors` with `longinteger` type. Sent errors.
- `/%{container_id}/txDropped` with `longinteger` type. Outgoing packets dropped.


### `/%{container_id}/interface`

Network interface name

Name of the network for which the statistics are provided.

This endpoint accepts values of type `string`: an UTF-8 string, at most 65536 bytes long.

The endpoint is parametric and `container_id` can be replaced with any valid string to send data on specialized paths.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Astarte expects a valid timestamp to be attached each time data is produced.
Data is considered delivered when the transport successfully sends the data regardless of the outcome.
Data is discarded if the transport is temporarily uncapable of delivering it.

### `/%{container_id}/rxBytes`

Bytes received.

Total number of bytes received on the interface.

This endpoint accepts values of type `longinteger`: a signed 64 bit integer (please note that longinteger is represented as a string by default in JSON-based APIs.).

The endpoint is parametric and `container_id` can be replaced with any valid string to send data on specialized paths.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Astarte expects a valid timestamp to be attached each time data is produced.
Data is considered delivered when the transport successfully sends the data regardless of the outcome.
Data is discarded if the transport is temporarily uncapable of delivering it.

### `/%{container_id}/rxPackets`

Packets received.

Total number of packets successfully received on the interface.

This endpoint accepts values of type `longinteger`: a signed 64 bit integer (please note that longinteger is represented as a string by default in JSON-based APIs.).

The endpoint is parametric and `container_id` can be replaced with any valid string to send data on specialized paths.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Astarte expects a valid timestamp to be attached each time data is produced.
Data is considered delivered when the transport successfully sends the data regardless of the outcome.
Data is discarded if the transport is temporarily uncapable of delivering it.

### `/%{container_id}/rxDropped`

Incoming packets dropped.

Total number of incoming packets that were dropped.

This endpoint accepts values of type `longinteger`: a signed 64 bit integer (please note that longinteger is represented as a string by default in JSON-based APIs.).

The endpoint is parametric and `container_id` can be replaced with any valid string to send data on specialized paths.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Astarte expects a valid timestamp to be attached each time data is produced.
Data is considered delivered when the transport successfully sends the data regardless of the outcome.
Data is discarded if the transport is temporarily uncapable of delivering it.

### `/%{container_id}/rxErrors`

Received errors.

Total number of errors that occurred while receiving.

This endpoint accepts values of type `longinteger`: a signed 64 bit integer (please note that longinteger is represented as a string by default in JSON-based APIs.).

The endpoint is parametric and `container_id` can be replaced with any valid string to send data on specialized paths.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Astarte expects a valid timestamp to be attached each time data is produced.
Data is considered delivered when the transport successfully sends the data regardless of the outcome.
Data is discarded if the transport is temporarily uncapable of delivering it.

### `/%{container_id}/txBytes`

Bytes sent.

Total number of bytes transmitted on the interface.

This endpoint accepts values of type `longinteger`: a signed 64 bit integer (please note that longinteger is represented as a string by default in JSON-based APIs.).

The endpoint is parametric and `container_id` can be replaced with any valid string to send data on specialized paths.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Astarte expects a valid timestamp to be attached each time data is produced.
Data is considered delivered when the transport successfully sends the data regardless of the outcome.
Data is discarded if the transport is temporarily uncapable of delivering it.

### `/%{container_id}/txPackets`

Packets sent.

Total number of packets successfully transmitted on the interface.

This endpoint accepts values of type `longinteger`: a signed 64 bit integer (please note that longinteger is represented as a string by default in JSON-based APIs.).

The endpoint is parametric and `container_id` can be replaced with any valid string to send data on specialized paths.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Astarte expects a valid timestamp to be attached each time data is produced.
Data is considered delivered when the transport successfully sends the data regardless of the outcome.
Data is discarded if the transport is temporarily uncapable of delivering it.

### `/%{container_id}/txErrors`

Sent errors.

Total number of errors that occurred while transmitting.

This endpoint accepts values of type `longinteger`: a signed 64 bit integer (please note that longinteger is represented as a string by default in JSON-based APIs.).

The endpoint is parametric and `container_id` can be replaced with any valid string to send data on specialized paths.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Astarte expects a valid timestamp to be attached each time data is produced.
Data is considered delivered when the transport successfully sends the data regardless of the outcome.
Data is discarded if the transport is temporarily uncapable of delivering it.

### `/%{container_id}/txDropped`

Outgoing packets dropped.

Total number of outgoing packets that were dropped.

This endpoint accepts values of type `longinteger`: a signed 64 bit integer (please note that longinteger is represented as a string by default in JSON-based APIs.).

The endpoint is parametric and `container_id` can be replaced with any valid string to send data on specialized paths.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Astarte expects a valid timestamp to be attached each time data is produced.
Data is considered delivered when the transport successfully sends the data regardless of the outcome.
Data is discarded if the transport is temporarily uncapable of delivering it.


## io.edgehog.devicemanager.apps.stats.ContainerProcesses v0.1

PidsStats contains Linux-specific stats of a container's process-IDs (PIDs).

### About

This interface is of type `datastream` and is owned by the `device`, meaning that it is the device which initiates the data flow.
Thanks to this type of interface, the device can send a mutable, ordered stream of data, with no concept of persistent state or synchronization.

Data gets sent with an `object` aggregation.
Astarte expects the owner to send all of the interface's mappings at the same time, packed in a single message.

### Mappings

The interface has the following mappings:

- `/%{container_id}/current` with `longinteger` type. Current is the number of PIDs in the cgroup.
- `/%{container_id}/limit` with `longinteger` type. Limit is the hard limit on the number of pids in the cgroup.


### `/%{container_id}/current`

Current is the number of PIDs in the cgroup.



This endpoint accepts values of type `longinteger`: a signed 64 bit integer (please note that longinteger is represented as a string by default in JSON-based APIs.).

The endpoint is parametric and `container_id` can be replaced with any valid string to send data on specialized paths.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Astarte expects a valid timestamp to be attached each time data is produced.
Data is considered delivered when the transport successfully sends the data regardless of the outcome.
Data is discarded if the transport is temporarily uncapable of delivering it.

### `/%{container_id}/limit`

Limit is the hard limit on the number of pids in the cgroup.



This endpoint accepts values of type `longinteger`: a signed 64 bit integer (please note that longinteger is represented as a string by default in JSON-based APIs.).

The endpoint is parametric and `container_id` can be replaced with any valid string to send data on specialized paths.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Astarte expects a valid timestamp to be attached each time data is produced.
Data is considered delivered when the transport successfully sends the data regardless of the outcome.
Data is discarded if the transport is temporarily uncapable of delivering it.


## io.edgehog.devicemanager.apps.stats.VolumeUsage v0.1

Statistics on the volumes

### About

This interface is of type `datastream` and is owned by the `device`, meaning that it is the device which initiates the data flow.
Thanks to this type of interface, the device can send a mutable, ordered stream of data, with no concept of persistent state or synchronization.

Data gets sent with an `object` aggregation.
Astarte expects the owner to send all of the interface's mappings at the same time, packed in a single message.

### Mappings

The interface has the following mappings:

- `/%{volume_id}/driver` with `string` type. Name of the volume driver used by the volume.
- `/%{volume_id}/mountpoint` with `string` type. Mount path of the volume on the host.
- `/%{volume_id}/createdAt` with `datetime` type. Date/Time the volume was created.
- `/%{volume_id}/usageDataSize` with `longinteger` type. Amount of disk space used by the volume (in bytes).
- `/%{volume_id}/usageDataRefCount` with `longinteger` type. The number of containers referencing this volume.


### `/%{volume_id}/driver`

Name of the volume driver used by the volume.



This endpoint accepts values of type `string`: an UTF-8 string, at most 65536 bytes long.

The endpoint is parametric and `volume_id` can be replaced with any valid string to send data on specialized paths.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Astarte expects a valid timestamp to be attached each time data is produced.
Data is considered delivered when the transport successfully sends the data regardless of the outcome.
Data is discarded if the transport is temporarily uncapable of delivering it.

### `/%{volume_id}/mountpoint`

Mount path of the volume on the host.



This endpoint accepts values of type `string`: an UTF-8 string, at most 65536 bytes long.

The endpoint is parametric and `volume_id` can be replaced with any valid string to send data on specialized paths.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Astarte expects a valid timestamp to be attached each time data is produced.
Data is considered delivered when the transport successfully sends the data regardless of the outcome.
Data is discarded if the transport is temporarily uncapable of delivering it.

### `/%{volume_id}/createdAt`

Date/Time the volume was created.



This endpoint accepts values of type `datetime`: a UTC timestamp, internally represented as milliseconds since 1st Jan 1970 using a signed 64 bits integer. (datetime is represented as an ISO 8601 string by default in JSON based APIs.)

The endpoint is parametric and `volume_id` can be replaced with any valid string to send data on specialized paths.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Astarte expects a valid timestamp to be attached each time data is produced.
Data is considered delivered when the transport successfully sends the data regardless of the outcome.
Data is discarded if the transport is temporarily uncapable of delivering it.

### `/%{volume_id}/usageDataSize`

Amount of disk space used by the volume (in bytes).



This endpoint accepts values of type `longinteger`: a signed 64 bit integer (please note that longinteger is represented as a string by default in JSON-based APIs.).

The endpoint is parametric and `volume_id` can be replaced with any valid string to send data on specialized paths.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Astarte expects a valid timestamp to be attached each time data is produced.
Data is considered delivered when the transport successfully sends the data regardless of the outcome.
Data is discarded if the transport is temporarily uncapable of delivering it.

### `/%{volume_id}/usageDataRefCount`

The number of containers referencing this volume.



This endpoint accepts values of type `longinteger`: a signed 64 bit integer (please note that longinteger is represented as a string by default in JSON-based APIs.).

The endpoint is parametric and `volume_id` can be replaced with any valid string to send data on specialized paths.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Astarte expects a valid timestamp to be attached each time data is produced.
Data is considered delivered when the transport successfully sends the data regardless of the outcome.
Data is discarded if the transport is temporarily uncapable of delivering it.


## io.edgehog.devicemanager.config.Telemetry v0.1



### About

This interface is of type `properties` and is owned by the `server`, meaning that it is the server which initiates the data flow.
Thanks to this type of interface, the server can set a persistent, stateful, synchronized state with no concept of history or timestamping.


### Mappings

The interface has the following mappings:

- `/request/%{interface_name}/enable` with `boolean` type. Enable/Disable telemetry update. Unset returns to the previous state configured in the device.
- `/request/%{interface_name}/periodSeconds` with `longinteger` type. Set interval of period seconds between the end of the previous update and the start of the next one. Unset returns to the previous state configured in the device.


### `/request/%{interface_name}/enable`

Enable/Disable telemetry update. Unset returns to the previous state configured in the device.



This endpoint accepts values of type `boolean`: either true or false, adhering to JSON boolean type.

The endpoint is parametric and `interface_name` can be replaced with any valid string to send data on specialized paths.

The value of the property can be unset.

### `/request/%{interface_name}/periodSeconds`

Set interval of period seconds between the end of the previous update and the start of the next one. Unset returns to the previous state configured in the device.



This endpoint accepts values of type `longinteger`: a signed 64 bit integer (please note that longinteger is represented as a string by default in JSON-based APIs.).

The endpoint is parametric and `interface_name` can be replaced with any valid string to send data on specialized paths.

The value of the property can be unset.


## io.edgehog.devicemanager.fileTransfer.DeviceToServer v0.1

File transfer from a Device to a Server

Request a file transfer operation. Providing an URL where the device will upload a file with an HTTP PUT request, the source of the file to upload is implementation specific.

### About

This interface is of type `datastream` and is owned by the `server`, meaning that it is the server which initiates the data flow.
Thanks to this type of interface, the server can send a mutable, ordered stream of data, with no concept of persistent state or synchronization.

Data gets sent with an `object` aggregation.
Astarte expects the owner to send all of the interface's mappings at the same time, packed in a single message.

### Mappings

The interface has the following mappings:

- `/request/id` with `string` type. Transfer ID for the file
- `/request/url` with `string` type. The URL to upload the file to
- `/request/httpHeaderKey` with `string` type. Keys for the HTTP headers, must be in the order of the values
- `/request/httpHeaderValue` with `string` type. Values for the HTTP headers, must be in the order of the keys
- `/request/compression` with `string` type. Compression to upload multiple files
- `/request/progress` with `boolean` type. Flag to enable the progress reporting of the download.
- `/request/source` with `string` type. Source for the file


### `/request/id`

Transfer ID for the file



This endpoint accepts values of type `string`: an UTF-8 string, at most 65536 bytes long.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Data is considered delivered when it has been received at least once by the recipient.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 3600 seconds before it is erased from the database.

### `/request/url`

The URL to upload the file to



This endpoint accepts values of type `string`: an UTF-8 string, at most 65536 bytes long.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Data is considered delivered when it has been received at least once by the recipient.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 3600 seconds before it is erased from the database.

### `/request/httpHeaderKey`

Keys for the HTTP headers, must be in the order of the values



This endpoint accepts values of type `string`: an UTF-8 string, at most 65536 bytes long.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Data is considered delivered when it has been received at least once by the recipient.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 3600 seconds before it is erased from the database.

### `/request/httpHeaderValue`

Values for the HTTP headers, must be in the order of the keys



This endpoint accepts values of type `string`: an UTF-8 string, at most 65536 bytes long.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Data is considered delivered when it has been received at least once by the recipient.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 3600 seconds before it is erased from the database.

### `/request/compression`

Compression to upload multiple files

Optional enum string for the file compression with default value empty, other values are: ['tar.gz']

This endpoint accepts values of type `string`: an UTF-8 string, at most 65536 bytes long.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Data is considered delivered when it has been received at least once by the recipient.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 3600 seconds before it is erased from the database.

### `/request/progress`

Flag to enable the progress reporting of the download.



This endpoint accepts values of type `boolean`: either true or false, adhering to JSON boolean type.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Data is considered delivered when it has been received at least once by the recipient.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 3600 seconds before it is erased from the database.

### `/request/source`

Source for the file

Device-specific field, some default values are storage and streaming.

This endpoint accepts values of type `string`: an UTF-8 string, at most 65536 bytes long.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Data is considered delivered when it has been received at least once by the recipient.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 3600 seconds before it is erased from the database.


## io.edgehog.devicemanager.fileTransfer.Progress v0.1

Progress of a file transfer.

If the request enabled progress reporting, the device will send the progress of the operation.

### About

This interface is of type `datastream` and is owned by the `device`, meaning that it is the device which initiates the data flow.
Thanks to this type of interface, the device can send a mutable, ordered stream of data, with no concept of persistent state or synchronization.

Data gets sent with an `object` aggregation.
Astarte expects the owner to send all of the interface's mappings at the same time, packed in a single message.

### Mappings

The interface has the following mappings:

- `/request/id` with `string` type. Transfer ID for the file
- `/request/progress` with `integer` type. Progress of the transfer in %


### `/request/id`

Transfer ID for the file



This endpoint accepts values of type `string`: an UTF-8 string, at most 65536 bytes long.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Data is considered delivered when the transport successfully sends the data regardless of the outcome.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 3600 seconds before it is erased from the database.

### `/request/progress`

Progress of the transfer in %



This endpoint accepts values of type `integer`: a signed 32 bit integer.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Data is considered delivered when the transport successfully sends the data regardless of the outcome.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 3600 seconds before it is erased from the database.


## io.edgehog.devicemanager.fileTransfer.Response v0.1

Response for a file transfer

Used by the device to report the transfer status upon completion. Used for both download and upload.

### About

This interface is of type `datastream` and is owned by the `device`, meaning that it is the device which initiates the data flow.
Thanks to this type of interface, the device can send a mutable, ordered stream of data, with no concept of persistent state or synchronization.

Data gets sent with an `object` aggregation.
Astarte expects the owner to send all of the interface's mappings at the same time, packed in a single message.

### Mappings

The interface has the following mappings:

- `/request/id` with `string` type. Transfer ID for the file
- `/request/code` with `longinteger` type. Success or error code for the transfer
- `/request/message` with `string` type. Optional message for the response


### `/request/id`

Transfer ID for the file

Can be either for download or upload transfers.

This endpoint accepts values of type `string`: an UTF-8 string, at most 65536 bytes long.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Data is considered delivered when it has been received at least once by the recipient.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 3600 seconds before it is erased from the database.

### `/request/code`

Success or error code for the transfer

A 0 code is a success, errors are POSIX errorno

This endpoint accepts values of type `longinteger`: a signed 64 bit integer (please note that longinteger is represented as a string by default in JSON-based APIs.).

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Data is considered delivered when it has been received at least once by the recipient.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 3600 seconds before it is erased from the database.

### `/request/message`

Optional message for the response



This endpoint accepts values of type `string`: an UTF-8 string, at most 65536 bytes long.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Data is considered delivered when it has been received at least once by the recipient.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 3600 seconds before it is erased from the database.


## io.edgehog.devicemanager.fileTransfer.posix.ServerToDevice v0.1

File transfer from a Server to a Device

Request a file transfer operation. Providing a URL from which the device will download a file with an HTTP GET request, the destination of the file to download is implementation specific.

### About

This interface is of type `datastream` and is owned by the `server`, meaning that it is the server which initiates the data flow.
Thanks to this type of interface, the server can send a mutable, ordered stream of data, with no concept of persistent state or synchronization.

Data gets sent with an `object` aggregation.
Astarte expects the owner to send all of the interface's mappings at the same time, packed in a single message.

### Mappings

The interface has the following mappings:

- `/request/id` with `string` type. Transfer ID for the file
- `/request/url` with `string` type. The URL to get the file from
- `/request/httpHeaderKey` with `string` type. Keys for the HTTP headers, must be in the order of the values
- `/request/httpHeaderValue` with `string` type. Values for the HTTP headers, must be in the order of the keys
- `/request/compression` with `string` type. Compression to upload multiple files
- `/request/fileSizeBytes` with `longinteger` type. File size decompressed
- `/request/progress` with `boolean` type. Flag to enable the progress reporting of the download.
- `/request/digest` with `string` type. Digest of the file contents
- `/request/fileName` with `string` type. Name of the file to download
- `/request/ttlSeconds` with `longinteger` type. TTL on how long to keep the file for
- `/request/fileMode` with `integer` type. Unix mode for the file
- `/request/userId` with `integer` type. Uid of the user owning the file
- `/request/groupId` with `integer` type. Gid of the user owning the file
- `/request/destination` with `string` type. Destination for the file


### `/request/id`

Transfer ID for the file

If the file is to be stored, this MUST be unique to the file (e.g. hash of the content). For a file that needs to be streamed, it can be unique for the single request (e.g. uuid).

This endpoint accepts values of type `string`: an UTF-8 string, at most 65536 bytes long.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Data is considered delivered when it has been received at least once by the recipient.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 3600 seconds before it is erased from the database.

### `/request/url`

The URL to get the file from



This endpoint accepts values of type `string`: an UTF-8 string, at most 65536 bytes long.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Data is considered delivered when it has been received at least once by the recipient.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 3600 seconds before it is erased from the database.

### `/request/httpHeaderKey`

Keys for the HTTP headers, must be in the order of the values



This endpoint accepts values of type `string`: an UTF-8 string, at most 65536 bytes long.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Data is considered delivered when it has been received at least once by the recipient.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 3600 seconds before it is erased from the database.

### `/request/httpHeaderValue`

Values for the HTTP headers, must be in the order of the keys



This endpoint accepts values of type `string`: an UTF-8 string, at most 65536 bytes long.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Data is considered delivered when it has been received at least once by the recipient.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 3600 seconds before it is erased from the database.

### `/request/compression`

Compression to upload multiple files

Optional enum string for the file compression with default value empty, other values are: ['tar.gz']

This endpoint accepts values of type `string`: an UTF-8 string, at most 65536 bytes long.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Data is considered delivered when it has been received at least once by the recipient.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 3600 seconds before it is erased from the database.

### `/request/fileSizeBytes`

File size decompressed

Total file size (if multiple files) uncompressed in bytes. It's used to reserve this space on the device.

This endpoint accepts values of type `longinteger`: a signed 64 bit integer (please note that longinteger is represented as a string by default in JSON-based APIs.).

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Data is considered delivered when it has been received at least once by the recipient.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 3600 seconds before it is erased from the database.

### `/request/progress`

Flag to enable the progress reporting of the download.



This endpoint accepts values of type `boolean`: either true or false, adhering to JSON boolean type.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Data is considered delivered when it has been received at least once by the recipient.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 3600 seconds before it is erased from the database.

### `/request/digest`

Digest of the file contents

Must be in the form sha256:deadbeaf, and should be used only if supported by the device.

This endpoint accepts values of type `string`: an UTF-8 string, at most 65536 bytes long.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Data is considered delivered when it has been received at least once by the recipient.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 3600 seconds before it is erased from the database.

### `/request/fileName`

Name of the file to download

Optional file name of the file to download, default is empty

This endpoint accepts values of type `string`: an UTF-8 string, at most 65536 bytes long.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Data is considered delivered when it has been received at least once by the recipient.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 3600 seconds before it is erased from the database.

### `/request/ttlSeconds`

TTL on how long to keep the file for

Optional ttl for how long to keep the file fore, if 0 is forever

This endpoint accepts values of type `longinteger`: a signed 64 bit integer (please note that longinteger is represented as a string by default in JSON-based APIs.).

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Data is considered delivered when it has been received at least once by the recipient.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 3600 seconds before it is erased from the database.

### `/request/fileMode`

Unix mode for the file

Optional unix mode for the file, set to default if 0. All files are immutable, so setting it to writable has no effect.

This endpoint accepts values of type `integer`: a signed 32 bit integer.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Data is considered delivered when it has been received at least once by the recipient.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 3600 seconds before it is erased from the database.

### `/request/userId`

Uid of the user owning the file

Optional unix uid of the user owning the file, set to default if -1.

This endpoint accepts values of type `integer`: a signed 32 bit integer.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Data is considered delivered when it has been received at least once by the recipient.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 3600 seconds before it is erased from the database.

### `/request/groupId`

Gid of the user owning the file

Optional unix gid of the group owning the file, set to default if -1.

This endpoint accepts values of type `integer`: a signed 32 bit integer.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Data is considered delivered when it has been received at least once by the recipient.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 3600 seconds before it is erased from the database.

### `/request/destination`

Destination for the file

Device-specific field, some default values are storage and streaming.

This endpoint accepts values of type `string`: an UTF-8 string, at most 65536 bytes long.

The endpoint has a specific configuration for how data is stored, transferred and indexed.
Data is considered delivered when it has been received at least once by the recipient.
Data is discarded if the transport is temporarily uncapable of delivering it.
Delivered data is kept for 3600 seconds before it is erased from the database.


## io.edgehog.devicemanager.storage.File v0.1

Property for the files stored on a device

Published when a file has been fully transferred and stored on the device.

### About

This interface is of type `properties` and is owned by the `device`, meaning that it is the device which initiates the data flow.
Thanks to this type of interface, the device can set a persistent, stateful, synchronized state with no concept of history or timestamping.


### Mappings

The interface has the following mappings:

- `/%{requestId}/pathOnDevice` with `string` type. Path on the device for the transferred file
- `/%{requestId}/sizeBytes` with `longinteger` type. Size in bytes of the file


### `/%{requestId}/pathOnDevice`

Path on the device for the transferred file



This endpoint accepts values of type `string`: an UTF-8 string, at most 65536 bytes long.

The endpoint is parametric and `requestId` can be replaced with any valid string to send data on specialized paths.

The value of the property cannot be unset.

### `/%{requestId}/sizeBytes`

Size in bytes of the file



This endpoint accepts values of type `longinteger`: a signed 64 bit integer (please note that longinteger is represented as a string by default in JSON-based APIs.).

The endpoint is parametric and `requestId` can be replaced with any valid string to send data on specialized paths.

The value of the property cannot be unset.


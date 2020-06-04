# Automatically collected information

The Experience Platform Mobile extension automatically collects and adds information to each Platform event that is sent to the Adobe Experience Platform. The following sections provide details about the collected information:

## Platform event

The [Experience Event](https://github.com/adobe/xdm/blob/master/docs/reference/context/experienceevent.schema.md) is a time-based record of an event. The XDM Experience Event schema is the top-level class for all Experience events and contains information about the event, device, environment, and the identity of the user. Here are the properties the Experience Platform Mobile extension automatically adds to each Platform event:

| Property  | Description                                                  |
| --------- | ------------------------------------------------------------ |
| Timestamp | The time when the event occurred. The timestamp is set when the Platform event is received by the Experience Platform Mobile extension. |
| ID        | A unique identifier for the time-series event.               |

## Identity

The [IdentityMap](https://github.com/adobe/xdm/blob/1c22180490558e3c13352fe3e0540cb7e93c69ca/docs/reference/context/identitymap.schema.md) defines a map that contains end-user identities. Here are the identity properties the Experience Platform Mobile extension automatically adds to each Platform event:

| Property | Description                                                  |
| -------- | ------------------------------------------------------------ |
| ECID     | The Experience Cloud Identifier (ECID)  that is generated by the Adobe Experiece Cloud Mobile SDK is added to the Platform event's `IdentityMap` . If the event contains an `IdentityMap` object, the ECID is added to the `IdentityMap` If the event does not contain the object, a new object is created and is added to the Platform event. |

## Device

[Device](https://github.com/adobe/xdm/blob/1c22180490558e3c13352fe3e0540cb7e93c69ca/docs/reference/context/device.schema.md) is included in the [Experience Cloud Environment details](https://github.com/adobe/xdm/blob/1c22180490558e3c13352fe3e0540cb7e93c69ca/docs/reference/context/experienceevent-environment-details.schema.md) mixin and details data about the mobile device. Here are the device properties that the Experience Platform Mobile extension automatically adds to each Platform event:

| Property           | Description                                                  |
| ------------------ | ------------------------------------------------------------ |
| Manufacturer       | The name of the organization that owns the design and creation of the device. |
| Model              | The name of the model for the device.                        |
| Model number       | The unique model number designation that is assigned by the manufacturer for this device. |
| Screen width       | The number of vertical pixels of the device's active display in its default orientation. |
| Screen height      | The number of horizontal pixels of the device's active display in its default orientation. |
| Screen orientation | The current screen orientation, and the options are portrait and landscape. |
| Type               | The type of device that is being tracked. The current options are phone and tablet. |

## Environment

[Environment](https://github.com/adobe/xdm/blob/1c22180490558e3c13352fe3e0540cb7e93c69ca/docs/reference/context/environment.schema.md) is included in the  [Experience Cloud Environment details](https://github.com/adobe/xdm/blob/1c22180490558e3c13352fe3e0540cb7e93c69ca/docs/reference/context/experienceevent-environment-details.schema.md) mixin and includes information about the surrounding environment at the time of the event. Here are the environment properties that the Experience Platform Mobile extension automatically adds to each Platform event:

| Property                 | Description                                           |
| ------------------------ | ----------------------------------------------------- |
| Carrier                  | A mobile network carrier.                             |
| Operating system         | The name of the operating system.                     |
| Operating system version | The full version identifier for the operating system. |





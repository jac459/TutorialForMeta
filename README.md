# Tutorial For Meta
## Focus on MQTT wiring.
Meta allows a lot of things and can be heavily programmed in order for example to build complex lists/directories with Neeo.
Yet, it can also used very simply to create/declare a driver and have it totally exposed through MQTT.

You can look at the driver TV.json. This driver is very simple, just declare a series of buttons, sliders, images, and labels, useful for a TV. There is no behaviors/intelligence coded here.
You can place this file in your meta/Active folder and when restarting meta, you will be able to find a "TV" meta device.

This device does nothing as such. But if you place an MQTT listener listening to meta/#, you will see that every time you interact with the driver, an MQTT message is sent. Likewise is you send an MQTT message to the same topic (but adding at the end "set"), you will be able to set the value in the driver directly.

This way, meta offers a way to fully control NEEO (not the list though) only by sending/receiving MQTT messages.

Full tutorial here:
https://youtu.be/_BDKjCqjjwo

### CAREFUL : Label, Sliders, Image CAN'T have a name with a space inside. This is only recommanded for buttons (for example "CURSOR UP" works for a Button but won't work for a label).

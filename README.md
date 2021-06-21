# hubitat_myLeviton

This provides Switch, SwitchLevel, and SignalStrength (wifi connection) driver capabilities for Hubitat with My Leviton Wi-Fi enabled switches and dimmers.

Note that all operations have a cloud (internet) interaction.  This implementation is based on the work shared here: <br>
https://gist.github.com/tlyakhov/4be20b588c4d34d9bd831c01c7594c92<br>
http://ihavenoknees.blogspot.com/2017/07/weekend-project-reverse-engineering.html<br>
https://github.com/tabrindle/homebridge-leviton/pull/9

# Installation instructions:

* In the *Drivers Code* section of Hubitat, add the myLevitonSystem and myLevitonSwitchDimmer drivers.
* In the *Devices* section of Hubitat, add a *New Virtual Device* of type My Leviton System.
* Open the configuration page for the newly created *Device* and enter your username and password for My Leviton and click *Save Preferences*.
* Refresh the configuration page and look for child devices for any switches or dimmers that are configured in your system.

# Usage instructions:

* Utilize the exposed switches and/or dimmers through any Hubitat app or extension.
* The states of switches or dimmers in child devices are updated when events are received from the My Leviton cloud.
    * These events occur regardless of how the switch or dimmer is adjusted -- whether it was physically pressed or through software control.  This driver attempts to determine the source and log the event type as either 'physical' or 'digital'.
    * You can also use the Refresh command on any child device or on the parent device to poll for updates.

# Disclaimer

I have no affiliation with any of the companies mentioned in this readme or in the code.  I also don't have any My Leviton enabled devices, so my ability to troubleshoot will be limited.


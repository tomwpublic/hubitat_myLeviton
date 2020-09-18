# hubitat_myLeviton

This provides Switch, SwitchLevel, and SignalStrength (wifi connection) driver capabilities for Hubitat with My Leviton Wi-Fi enabled switches and dimmers.

Note that all operations have a cloud (internet) interaction.  This implementation is based on the work shared here: <br>
https://gist.github.com/tlyakhov/4be20b588c4d34d9bd831c01c7594c92<br>
http://ihavenoknees.blogspot.com/2017/07/weekend-project-reverse-engineering.html

# Installation instructions:

* In the *Drivers Code* section of Hubitat, add the myLevitonSystem and myLevitonSwitchDimmer drivers.
* In the *Devices* section of Hubitat, add a *New Virtual Device* of type My Leviton System.
* Open the configuration page for the newly created *Device* and enter your username and password for My Leviton and click *Save Preferences*.
* Refresh the configuration page and look for child devices for any switches or dimmers that are configured in your system.

# Usage instructions:

* Utilize the exposed switches and/or dimmers through any Hubitat app or extension.
* Note that the states of switches or dimmers in child devices are refreshed from the master at a fixed interval.  Adjust the *Refresh interval (minutes)* input on the My Leviton System device as needed.

# Disclaimer

I have no affiliation with any of the companies mentioned in this readme or in the code.  I also don't have any My Leviton enabled devices, so my ability to troubleshoot will be limited.


# A collection of meta-Plus drivers

## Latest additions/revisions: 
### Tasmota.json
A driver to control Tasmota devices. This is a complete revision of the previous one. That one was using a complicated set of MQTT-calls supported by an older version of Tasmota.MQTT integration.
This version uses the latest Tasmota integration. It requires the command SetOption19 0 to be executed on the Tasmota device console. The MQTT-broker used is hardcoded as all of my MQTT-devioces connect top a dedicated mosquito-container. Simpoly chanmge 192.168.73.24 to the IPaddress of your your MQ-broker. If I receive request to make this dynamic too, I can look into that (if time permits).
### Tasmota.json
A driver to control Tasmota devices in the old style. 
This is a complete revision of the previous one. It supports the old style (protocol) Tasmota/MQTT integration that is activated by executing the command SetOption19 1 to be executed on the Tasmota device console.

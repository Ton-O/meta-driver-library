# A collection of meta-Plus drivers

## Latest additions/revisions: 
### Tasmota.json
A driver to control Tasmota devices. This is a complete revision of the previous one. That one was using a complicated set of MQTT-calls supported by an older version of Tasmota.MQTT integration.
This version uses the latest Tasmota integration. It requires the command SetOption19 0 to be executed on the Tasmota device console. The MQTT-broker used is hardcoded as all of my MQTT-devioces connect top a dedicated mosquito-container. Simpoly chanmge 192.168.73.24 to the IPaddress of your your MQ-broker. If I receive request to make this dynamic too, I can look into that (if time permits).
### Tasmota.json
A driver to control Tasmota devices in the old style. 
This is a complete revision of the previous one. It supports the old style (protocol) Tasmota/MQTT integration that is activated by executing the command SetOption19 1 to be executed on the Tasmota device console.

## Update 2025-02-24: Broadlink driver revised
Totally redesigned Broadlink driver. An example of the use of that driver is 32PFL5206H.json (a driver for Philips TV) which shows how to use that new driver functionality.
Meta Plus was using the excellent library python-broadlink from mjg59 to control your Broadlink devices.
To call the function in the python-broadlink library from the Javascript based Meta Plus, an intermediate Python module was the glue between Meta Plus and that external library.
Though stable, the use of Python was always a bit of a "strange duck in the pond".
This driver and its associated rework in Meta Plus is now complete Javascript based, so no python-stuff anymore.
This introduces the package node-broadlink and removes the package python-broadlink from mjg59
It goes without saying that this dri ver functionality will only work with Meta Plus level 3.7 and up.

## Update 2025-02-25: KODI-V2 released
KODI-V2 is the same driver as KODIPlayer, but with a different discover functionality: avahi in-stead of dnssd.
Lately I noticed that discovery of previously working KODI-systems (I use KODI on Chromecast with GoogleTV) stopped working: they simply couldn't be found anymnore. The reason.... tough one... It looks thas if the latest firmware for Chromecast cwith GoogleTV stopped advertisement of some services; KODI being one of them.
If your current KODI-systems still work, don't consider changing to this version as there is no need. But if you experience issues with discovery of KODI-devices, do consider switching. 
I will keep both versions of KODI driver oin sync: KODI.json and Kodi-V2) in my Meta driver library. 

## Update 2025-02-25: Some fixes in metaCore.json


## My META/NEEO related repositories
[Meta Brain])(https://github.com/Ton-O/MetaBrain)
[Meta Plus])(https://github.com/Ton-O/NEEO-Meta-Plus)
[Meta driver Library])(https://github.com/Ton-O/meta-driver-library)
[Docker image neeobrain](https://hub.docker.com/r/tonot1/neeobrain)
[Docker image neeo-meta-plus](https://hub.docker.com/r/tonot1/neeo-meta-plus)
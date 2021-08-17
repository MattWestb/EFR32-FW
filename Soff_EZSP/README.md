## Soff EZSP

Configuration Parameter | Value
-- | --
Module | SM-011
Part | EFR32MG21A020F768IM32
Version | EZSP 6.9.2.0
Status |  Untested
Address Table Size | 8
Child Table Size | 32
Source Routes | 7
CTUNE value | 128
TX | PB01
RX | PB00
CTS | ?
RTS | ?
BTL | PA00 (Low = BTL boot)
LED | PC00 

SonOff ZBB and USB dongle can using the same firmware but the ZBB is standard locked and need one signed firmware if not flashing one new bootloadre with SWD.  
Both have large problems with hardware and the chip / module is not clibrated from the factory and need patching the firware with CTune for working.

### EZSP six ten

NCP with GP, Multirail, NVM3, Max TC Link keys and Tube013 pro setting.  
  
Extra setting that Tube013 dont have:  
GP_SINK_TABLE_SIZE = 100  
GP_PROXY_TABLE_SIZE = 100  
KEY_TABLE_SIZE = 127  
CTUNE = 128

Not configured: LED and Button then its for the Sonoff ZBB that is flashed with SWD but working on Zigbee Stick.  
Its is using NVM3 so shall being flashed with S37 file for alocating the NVM3 aria OK ("normal" is using SIMM2 key storage and is making one new self if needed).  
This is very exprimental and 110% only for devs then six ten is having new toolshange and have many new bugs !!!  
   
EZSP 6.10.0.0 (six ten) is having one extra fix for CTune problems on MG21 devices so is interesting if it can helping with the "Sonoff problems". 
  
  
### Soff EZSP Router
  
Configuration Parameter | Value
-- | --
Module | SM-011
Part | EFR32MG21A020F768IM32
Version | EZSP 6.10.1.0
Status |  Untested
CTUNE value | 128
TX | PB01
RX | PB00
BTL | PA00 (Low = BTL boot)
NA | PA01 (dummy for compilling the plugin)
LED | PC00 
  
  
From the pluging description:
> (Requires Network Creator Security + Network Creator or Network Steering plugin to function properly in Zigbee 3.0 networks. Else, Network Find plugin is strongly recommended but not mandatory.) This code will hook up button 0 to have specific behavior based on the current network state. The behavior is as follows. If the device is not joined to a network, it will form a Zigbee 3.0 network (via Network Creator plugin) if it is configured as a coordinator or join a Zigbee 3.0 or ZHA legacy network (via Network Steering plugin) if it is configured as a router. If the device is joined to a network then pressing the button will broadcast a ZDO permit join to allow new devices to join. Holding the button for 5 seconds and releasing will cause the device to leave the network. Button 1 is not used and a callback is provided to another module wishing to use it.  
  
Compleet CLI with help is in the firmware for debug and also joining / leaving the network from CLI.
I recomending doing one chip erase and flashing one bootlooader and then the router S37 firmware but i attaticg the GBL if like trying doing it without erasing the flash.  
Pins is taken from the USB Stick that have the same pins plus one LED and shall working the same.  
The joining pin is the same as being used for bootloader so possible using it in Tasmota or ESPHome as switches.  

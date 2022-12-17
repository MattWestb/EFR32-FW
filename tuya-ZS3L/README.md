ncp-gp-LDMG21-92.s37 = MG21 NCP with GP and SW folw control and NVM3 EZSP 6.9.2.0.  
ncp-gp-LDMG21-10.s37 = MG21 NCP with GP and SW folw control and NVM3 EZSP 6.10.0.0.


## TUYA ZS3L

Configuration Parameter | Value | Pin/Pad
-- | -- | --
Module | tuya | ZS3L
Part | EFR32MG21A020F768IM32-B
Version | EZSP 6.9.2.0 / 6.10.0.0
Type | NCP-NVM3-GP-SW / NCP-NVM3-GP-SW-10
Status | Working / Untested
Address Table Size | 8 / 32 | ST / NT
Child Table Size | 32 | ST
Source Routes | 7 / 100 | ST / NT
Green Power Proxy Table Size | 100 | ST
Green Power Sink Table Size | 100 | ST
NVM3 Flash Pages | 12 | NS
Link Key Table Size | 127 | NS
CTUNE value | -1 | ST
PTI | Enabled
VUART | Enabled
VCC | 3.3 V | 1
GND | GND| 2
RX NCP / VCom | PA06 | 3
TX NCP / VCom | PA05 | 4
PTI Frame | PD01 | 5
PTI Data | PD00 | 6
SWCLK | PA01 | 7
SWDIO | PA02 | 8
SWO | PA03 | 9
Reset | Rest | 10
BLP | PC02 | -


First out :-))
```
EmberZNet version: 6.10.0.0 build 169
```
## rcp-uart-802154
Addnig one working rcp for the ZS3L.  
Pinout is standard tuya so RX = PA06 and TX = PA05.  
Use socket://192.168.2.64:9999 (with your HAS IP address) and 115200 baud in the addon.  
HA is up and running with one 
```
Device info
LEPTITER Recessed spot light
by IKEA of Sweden
```
Mor testing is comming and if going well all my test networks is being moved if all devices is liking the new coordinator.  
Little OT info (little patched):
```
IPv6:LocalAddress
fd11:XX:0:0:8cc0:XXXX:6685:7f35

IPv6:MeshLocalAddress
fdce:XXXX:604a:XXXX:2706:XXXX:c718:62ec

IPv6:MeshLocalPrefix
fdce:XXXX:604a:XXXX:

Network:Name
OpenThreadMWTest

OpenThread:Version
OPENTHREAD/9e70b13f-dirty; POSIX; Feb 24 2022 14:27:39

RCP:Version
SL-OPENTHREAD/2.0.1.0_GitHub-55af6ce2c; EFR32; Mar 6 2022 11:11:28
```
Sadly my nighburs dont have any OT devices online so im being very alone ;-((  
  
RCP 4.2.0.0 updated in Zip file with bootloader. The 23 HW is working OK for my with the latest HA addon and ZHA.


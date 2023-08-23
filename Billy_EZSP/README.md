IKEA ICC-A-1 module "Billy EZSP"

## Billy EZSP
Standard pin/pad/setting for NCP.
Configuration Parameter | Value | Pin/Pad
-- | -- | --
Module | IKEA | ICC-A-1
Part | EFR32MG1P132F256IM32
Version | EZSP 6.10.3.0 and 6.10.7.0
Type | NCP SW / NCP GP Multirail NVM3
Status |  Un / minimal tested
Address Table Size | 8 / 100 | ST / NS
Child Table Size | 32 / 16 | ST / NS
Source Routes | 7 / 64 | ST / NS
Link Key Table Size	| 127	| NS
CTUNE value | -1 | ST
DC-DC | True | NS
VCC | 3.3 V  | 1
GND | GND| 2
RX NCP / VCom | PB15 | 3
TX NCP / VCom | PB14 | 4
PTI Frame / CTS | PC10 | 5
PTI Data / RTS | PC11 | 6
SWCLK | PF0 | 7
SWDIO | PF1 | 8
SWO | PF2 | 9
Reset | Rest | 10
BLP | PA0 | -


## Billy Zigbee Router 
EZSP 6.9.2.0 Router with joining / leaving with pairing button if being used on one E1743 remote.  
Debug CLI is on the normal RX and TX pins so software leaving and joining is also possible CLI commands.  
PTI is enabled if running on havrdware that have this pads / pins.  
Button funktion:

>(Requires Network Creator Security + Network Creator or Network Steering plugin to function properly in Zigbee 3.0 networks.  Else, Network Find plugin is strongly recommended but not mandatory.)  This code will hook up button 0 to have specific behavior based on the current network state.  The behavior is as follows. If the device is not joined to a network, it will form a Zigbee 3.0 network (via Network Creator plugin) if it is configured as a coordinator or join a Zigbee 3.0 or ZHA legacy network (via Network Steering plugin) if it is configured as a router. If the device is joined to a network then pressing the button will broadcast a ZDO permit join to allow new devices to join.  Holding the button for 5 seconds and releasing will cause the device to leave the network.  Button 1 is not used and a callback is provided to another module wishing to use it.

## Six ten
Mullti rail NCP with GP (50 devices) and NVM3 with 127 TC link keys EZSP 6.10.3.0. and 6.10.7.   
The 6.10.7 both HW and SW and the last is having PTI and the first one not then the same pins in being used for HW.   
I was updating with WSDK and was erasing the NVM but ZHA was restroing it after some problems and my production network looks working well after some minutes and i keep looking on it for some days.  Up and running in production system for some day and looks being OK !!

## ZBCB 6.9.2.0
One Zigbee Control Bridge with EP 1 is one Control Bridge and EP 2 is one Color Dimmebal Light.
Using standard Billy RX and TX with full CLI and help and the light can being added to more groups and you is also recieving the group commands being sent to the group and broadcast to bonded group / device or unicat to device or group cast of commands from the CLI to the mesh :-)).  
 
## Billy rcp 802154
Billy-rcp-uart-802154-412-115200.s37 with standard pining but only v.com no PTI and no flow control is working OK.  
You need haveing one working bootloader flashed or the RCP is not starting that also included inthe zip file with 230400 and 460800 versions.    



![BillyRCP01](https://user-images.githubusercontent.com/49618193/161375800-ae4260cf-14f1-417b-b294-d199a8eaa635.PNG)
And Billy is running EZSP 7 !!!

![Seven](https://user-images.githubusercontent.com/49618193/161375855-3f13dfa8-e381-4d16-95f6-347d1f283815.png)
Was readeing little more and its looks SW flow controll is not implanted in GSDK 4 and in the end i think its useless running it on the SOC / chip then its only having 256K flash.  
More testig  is needed and also getting RCP working on Markus.  
   
 RCP 4.2.0.0 uploaded with all baudrate and with  HW and without fllow control.
 I have testing 11NF, 11 HW and 23HW and working OK with latest HA addon.
 ```
 2022-12-16 12:51:55.659 INFO (MainThread) [bellows.zigbee.application] EmberZNet version: 7.2.0.0 build 0
```
So Billy is running seven two :-)))  
  
Updated RCP to 4.2.1.0 then many bug fixes also for the leaving direct children is in and the 4.1.4.0 is having com problms on all my test installations (CRC failur on sending to the RCP).  
RCP 4.2.1.0 uploaded, i using 115K NF and 230K HW and looks working OK on Billy.  
  
Udated RCP 4.2.2.0 that looks working OK and is using the same RCP protocol version (V3) as 4.2.1.0 and both is working with addon 1.0.1 and 1.0.2.   
  
Udated RCP 4.3.0.0    
And RCP 4.3.1.0 (Woeks great with latest HA addon and it getting EZSP 7.3.1.0 in ZHA !!!)

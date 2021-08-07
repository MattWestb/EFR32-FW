IKEA ICC-A-1 module "Billy EZSP"

## Billy EZSP
Standard pin/pad/setting for NCP.
Configuration Parameter | Value | Pin/Pad
-- | -- | --
Module | IKEA | ICC-A-1
Part | EFR32MG1P132F256IM32
Version | EZSP 6.9.2.0 / 6.10.0.0
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
PTI Data | PC10 | 5
PTI Frame | PC11 | 6
SWCLK | PF0 | 7
SWDIO | PF1 | 8
SWO | PF2 | 9
Reset | Rest | 10
BLP | PA0 | -


ZigbeeBillyRouter = EZSP 6.9.2.0 Router with joining / leaving with pairing button if being used on one E1743 remote.  
Debug CLI is on the normal RX and TX pins so software leaving and joining is also possible CLI commands.  
PTI is enabled if running on havrdware that have this pads / pins.  
Button funktion:

>(Requires Network Creator Security + Network Creator or Network Steering plugin to function properly in Zigbee 3.0 networks.  Else, Network Find plugin is strongly recommended but not mandatory.)  This code will hook up button 0 to have specific behavior based on the current network state.  The behavior is as follows. If the device is not joined to a network, it will form a Zigbee 3.0 network (via Network Creator plugin) if it is configured as a coordinator or join a Zigbee 3.0 or ZHA legacy network (via Network Steering plugin) if it is configured as a router. If the device is joined to a network then pressing the button will broadcast a ZDO permit join to allow new devices to join.  Holding the button for 5 seconds and releasing will cause the device to leave the network.  Button 1 is not used and a callback is provided to another module wishing to use it.

## Six ten
Mullti rail with GP (50 devices) and NVM3 with 127 TC link keys.

## ZBCB 6.9.2.0
One Zigbee Control Bridge with EP 1 is one Control Bridge and EP 2 is one Color Dimmebal Light.
Using standard Billy RX and TX with full CLI and help and the light can being added to more groups and you is also recieving the group commands being sent to the group and broadcast to bonded group / device or unicat to device or group cast of commands from the CLI to the mesh :-)).

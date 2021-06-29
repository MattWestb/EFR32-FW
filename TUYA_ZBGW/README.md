## TUYA TYGWZ01

Configuration Parameter | Value | Pin/Pad
-- | -- | --
Module | tuya | TYZS4
Part | EFR32MG1B232F256GM48-D
Version | EZSP 6.9.2.0 / 6.10.0.0
Status |  Untested / Untested
Address Table Size | 8 | ST
Child Table Size | 32 | ST
Source Routes | 7 | ST
CTUNE value | -1 | ST
DC-DC | True | NS
VCC | 3.3 V | 1
GND | GND| 2
RX NCP / VCom | PA01 | 3
TX NCP / VCom | PA00 | 4
PTI Frame | PB12 | 5
PTI Data | PB13 | 6
SWCLK | PF0 | 7
SWDIO | PF1 | 8
SWO | PF2 | 9
Reset | Rest | 10
BLP | PA2 | -
CTS | PA5 | -
RTS | PA4 | -

## EZSP Six ten 

Mutirail, GP, NVM3, and  Max TC Link keys

Configuration Parameter | Value | 
-- | -- | 
AF_PLUGIN_NVM3_FLASH_PAGES | 9
GP_SINK_TABLE_SIZE | 50
GP_PROXY_TABLE_SIZE | 50
KEY_TABLE_SIZE | 127
REQUEST_KEY_TIMEOUT | 3
SOURCE_ROUTE_TABLE_SIZE | 64
APS_UNICAST_MESSAGE_COUNT | 32
MAX_END_DEVICE_CHILDREN | 16
PACKET_BUFFER_COUNT | 64
BROADCAST_TABLE_SIZE | 32
NEIGHBOR_TABLE_SIZE | 26
ADDRESS_TABLE_SIZE | 164

For not running out of flash and RAM is the NVM3 pages and APS_UNICAST_MESSAGE_COUNT redues for fitting in the hardware.  
Parametes not changed is left at defalt valiue.  


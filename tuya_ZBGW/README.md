## TUYA TYGWZ01

Configuration Parameter | Value | Pin/Pad
-- | -- | --
Module | tuya | TYZS4
Part | EFR32MG1B232F256GM48-D
Version | EZSP 6.10.3.0 / 6.10.7.0
Status |  Minimal tested
Address Table Size | 8 | ST
Child Table Size | 32 | ST
Source Routes | 7 | ST
CTUNE value | -1 | ST
DC-DC | True | NS
VCC | 3.3 V | 1
GND | GND| 2
RX NCP / VCom | PA01 | 3
TX NCP / VCom | PA00 | 4
CTS | PA05 | 5
RTS | PA04 | 6
SWCLK | PF00 | 7
SWDIO | PF01 | 8
SWO | PF02 | 9
Reset | Rest | 10
BLP | PA02 | -
PTI Frame | PB12 | Ext1
PTI Data | PB13 | Ext2

## EZSP Six ten 

Mutirail, GP, NVM3, and  Max TC Link keys

Configuration Parameter | Value | 
-- | -- | 
AF_PLUGIN_NVM3_FLASH_PAGES | 8
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
ADDRESS_TABLE_SIZE | 64

For not running out of flash and RAM is the NVM3 pages and APS_UNICAST_MESSAGE_COUNT redues for fitting in the hardware.  
Parametes not changed is left at defalt valiue.  

Have posting the later EZSP 6.10.7.0 and our Danish firends have reporting its working well but its not well tested but many bugs and security fixes is in it so recomended for testing and is canidate for stable firmware for the ZBGW.  
EZSP 6.10.8.0 with new bootloader (1.12.4) that shall being fixed and is ZERO tested.  
  
## RCP 4.2.0.0
Booting OK and can connecting with USF but not tested with HA addon.  
If getting problem you is likely need erasing the flash (with SWD) and flashing new bootloader and APP for recover so be carful !!
I have RCP 4.3.1.0 up and running for some week on my Billis and shall trying cooking one more time for theis module but its coming later and i posting then i have somthing for testing (SWD probe needed for the first round if not working).

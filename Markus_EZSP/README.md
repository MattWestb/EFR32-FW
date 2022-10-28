IKEA 3 gen Zigbee devices is using one original Silabs MGM210LA22JNF2 that is pre certificated and calibrated from the factory.  
My code name is "IKEA Markus EZSP".  
   
My pinout is the same as Billy: 

| MW pin | Modul pad | EFR32 pins | Description |
|--------|-----------|------------|-------------|
| 1      | VDD       | VDD        | 3.3V        |
| 2      | GND       | GND        | GND         |
| 3      | 7         | PC01       | RX          |
| 4      | 8         | PC00       | TX          |
| 5      | 18        | PC05       | PTI Frame / Sync / RTS  |
| 6      | 17        | PC04       | PTI Dout / Data / CTS  |
| 7      | 1         | PA1        | SWCLK       |
| 8      | 2         | PA2        | SWDIO       |
| 8      | 3         | PA3        | SWO         |
| 10     | 11        | RESET      | Target reset | 
| NA     | 9         | PD01       | Boot Loader Pin |

Force bootloader pin PD01 is defined but noramaly not needed then using software command and then using WSTK for debricking the chip is only the resert pin needed.  
  
### Firmware settings.
Configuration Parameter | Value | Pin/Pad
-- | -- | --
Module | Silabs| MGM210LA22JNF2
Version | EZSP | 6.10.3.0
Type | NCP-NVM3-GP-SW
Status | Minimal tested
Address Table Size |32 | NS
Child Table Size | 32 | ST
Source Routes |100 | NS
Green Power Proxy Table Size | 100 | ST
Green Power Sink Table Size | 100 | ST
NVM3 Flash Pages | 12 | NS
Link Key Table Size | 127 | NS
CTUNE value | -1 | ST
PTI | Enabled
VUART | Enabled
  
Bootloaader and NCP is minmal tested but looks working OK.  
  
I have cooking one RCP for Zigbee and OpenThread multiprotocol add-on but i was upgrading my Armbian and have broken the install so i cant  testing it at all :-(((   
Also its looks Silabs have not implanted software flow controll and also messing with  the EZSP install for the module so i cant getting one EZSP 7 working (its working then its alocating NVM in the flash but no comunication with the host if can getting it compilled).

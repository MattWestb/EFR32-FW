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

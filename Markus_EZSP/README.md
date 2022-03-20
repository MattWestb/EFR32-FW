IKEA 3 gen Zigbee devices is using one original Silabs MGM210LA22JNF2 that is pre certificated and calibrated from the factory.  
My code name is "IKEA Markus EZSP".  
   
My pinout is the same as Billy: 

| MW pin | Modul pad | EFR32 pins | Description |
|--------|-----------|------------|-------------|
| 1      | VDD       | VDD        | 3.3V        |
| 2      | GND       | GND        | GND         |
| 3      | 7         | PC01       | RX          |
| 4      | 8         | PC00       | TX          |
| 5      | 18        | PC05       | PTI Frame / Sync   |
| 6      | 17        | PC04       | PTI Dout / Data    |
| 7      | 1         | PA1        | SWCLK       |
| 8      | 2         | PA2        | SWDIO       |
| 8      | 3         | PA3        | SWO         |
| 10     | 11        | RESET      | Target reset | 
| NA     | 9         | PD01       | Boot Loader Pin |

Force bootloader pin PD01 is defined but noramaly not needed then using software command and then using WSTK for debricking the chip is only the resert pin needed.

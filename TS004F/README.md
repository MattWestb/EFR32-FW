Dummped main flash and user data in bin format.

From J-Flasher:
```
Reading entire flash chip ...
 - 97 sectors, 2 ranges, 0x0 - 0xBFFFF, 0xFE00000 - 0xFE003FF
```
This one was trickey then Silabs Commander was not like reading all data from the device info (secure elements status) but was possible reading the "flash map".
![TS004F01](https://user-images.githubusercontent.com/49618193/138747974-a226f5f4-b657-45cd-a782-d5ff6a7ff280.PNG)

And its have only little flash used for the code:

![TS004F02](https://user-images.githubusercontent.com/49618193/138748150-fe8f08e8-adcb-4916-9004-12d11d6b679f.PNG)

I think the chip is not locked but without the reset it was not possible talking with the device but with other with the same zigbee module (ZS3L) was OK so i think its some components on the PCB like LEDs is conecting to one of the SWD pins that is making it trickey to cominucating with over SWD.

Interesting is that all noraml manufactur tockens is empty in the user data but tuya have adding little data at the end that is normally not used of the Silabs standard code:
```
fL4u„Wrü69É¥bdSÀÚ6 öbŸjÏZn…òÑò$2ž˜0ë
```
Flash token for the device cominucating with tuya cloud ?

I dont have some schematic of the PCB but they is using 4 inpits for switches and 4 outputs for LEDs and the PCB is black and cant looking thrue it in strong light,

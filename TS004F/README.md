Dummped main flash and user data in bin format.

From J-Flasher:
```
Reading entire flash chip ...
 - 97 sectors, 2 ranges, 0x0 - 0xBFFFF, 0xFE00000 - 0xFE003FF
```
Interesting is that all noraml manufactur tockens is empty in the user data but tuya have adding little data at the end that is normally not used of the Silabs standard code:
```
fL4u„Wrü69É¥bdSÀÚ6 öbŸjÏZn…òÑò$2ž˜0ë
```
Flash token for the device cominucating with tuya cloud ?

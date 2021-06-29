All EFR32 chips have one dictated aria in the flash for user data named `userdata`.  
Its stors some mandufactur tokens and also cunstom tokens.  
Its not being erased of debug unlock / flash erase andd firmware flashing. Chip ease and writing "erase" as token data is deleting it or writing it new updated token.   
IKEA is using it to storing cuntom token with overriding the mdele ID and other parameters that is in the firmware for using the same firmware for mor products like the 5 buttom remotes have the same firmware but diferent names.  

For NCP firmware you can storing some of the tokens and bellows / ZHA is readding them and you iss getting in the log.  

You can writing token one by one or more from one file.  
You can writing them to chip (flashing the chip with new tokens) or appanding them to one firmware that is flasing the firmware and the new tokens.  


Example of tocken file:
```
MFG_STRING                    : "IKEA of Sweden"
MFG_BOARD_NAME                : "Billy EZSP by MW"
MFG_MANUF_ID                  : 0x110C
```
And flashing the token file with simplicity commander:
```
.\commander.exe flash --tokengroup znet --tokenfile .\tokens-MW.txt -d EFR32MG1P132F256IM32
WARNING: The string for token MFG_BOARD_NAME (Billy EZSP by MW) fills all 16 bytes of the token space. The string will not be zero terminated.
Writing 2048 bytes starting at address 0x0fe00000
Comparing range 0x0FE00000 - 0x0FE007FF (2 KB)
Erasing range 0x0FE00000 - 0x0FE007FF (1 sector, 2 KB)
Programming range 0x0FE00000 - 0x0FE001FF (512 Bytes)
Programming range 0x0FE00200 - 0x0FE003FF (512 Bytes)
DONE
```
You is getting this from bellows info:
```
Manufacturer: IKEA of Sweden
Board name: Billy EZSP by MW
EmberZNet version: 6.9.0.0 build 178

```
The same shall working with this commands for appending the token to one firmware file:
>$ commander convert blink.s37 --tokengroup znet --tokenfile tokens.txt --device EFR32MG1P --outfile blink.hex Converts blink.s37 to hex format, while simultaneously defining the tokens defined in tokens.txt and on the command line.

Only putting your parameters for your chip and the in and output file.  

Editing: Its looks its only possible using the "flash" or "convert" s37 to s37 fils and adding the tokens but to GBL is not working and if having one s37 file with tokens and converting / craating one GBL its only taking the app and not the extra data for the tokens.
I think that is made for not being possible "streeling" devices without having hw access to them (= SWD flashing).

Alos if you is having one IKEA device hockedup you shall dumping the user airia that can being used for "transforming" one device if you like.  
The main firmware can beeing restored from one OTA filee but not the user data so all dumps of its is wery wellcome in the comunity for firmware transforming.

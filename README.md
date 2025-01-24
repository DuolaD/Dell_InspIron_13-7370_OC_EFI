# Dell_InspIron_13-7370_OC_EFI
A Opencore EFI for Dell InspIron 13-7370.

PLEASE READ ALL DETAILS IN README.MD BEFORE YOU DOWNLOAD EFI ON RELEASES.  

> [!NOTE]
> ·Only tested on MacOS 15.2 Sequoia. Might be support MacOS 13.X Ventura to 15.X Sequoia. Test by yourself.

> [!Warning]
> ·BEFORE YOU BEGIN,Go TO BIOS(click F2 when laptop started before boot to system) AND GO TO 'Security' TO SET 'PTT OFF'/SET 'TPM 2.0 Security' ENABLED.IF BIOS WARNING 'error,PTT cannot be enabled with legacy option roms enabled',GO TO 'Advanced Boot Opinion' AND ENABLED 'Enable Attempt Legacy Boot.'.THEN TRY AGAIN AND SAVE SETTINGS AND EXIT BIOS.
> 
> ·This laptop can not use with Broadcom Inc. network card, And EFI not support it. This EFI only support Intel Inc. network card.
>   
>  This is because if you try modify config.plist to add support, during startup, Intel CPU build-in GPU/hard disk/network card will crashed and generate a lot of random errors let systeam suck.

Support those Intel Inc. network card (Original Intel Inc. network card is on the list, but performance is too bad, I recommend replace it.):  
（1）DVM 1000 Series ~ 6000Series. like Intel(R) Centrino(R) Advanced-N 6205 AGN.  
（2）MVM 7000 Series ~ 9000 Series. like Intel(R) Dual Band Wireless AC 8260.  
（3）MVM Gen 2 22000 Series. like Intel(R) Wireless-AC 9270 160MHz、Intel(R) Wi-Fi 6 AX211 160MHz.  
（4）MVM Gen 3 22000 Series. like Intel(R) Wireless-AC 9560 160MHz、Intel(R) Wi-Fi 6 AX210 160MHz.  

You need to connect wired LAN after you success login system,then [download OCLP](https://github.com/dortania/OpenCore-Legacy-Patcher) and install + run.  
Then click 'Post-Install Root Patch' and install to add Intel Inc. network card support on MacOS.Then reboot, Done.  

Intel Inc. network card not support Airdrop(In some MacOS, it can't use full function), Relay, or Sidecar.  

Support those hard disk (Original hard disk(Sandisk X200 M2 SATA) is on the list. If you want to change hard disk, follow the list below. ):  
· All hard disk that run with SATA protocol.  
· All hard disk that releases by Western Digital Inc.   
· All hard disk that master is releases by PHISON Inc./Maxio Inc.  

DO NOT REPLACE ANY KIND OF HARD DISK AT THE LIST BELOW(Unless it run with SATA protocol.):  
· All hard disk releases by Samsung Inc.  
· All hard disk that master is releases by Micron Inc./SK Hynix Inc./YingRen Inc.  

After installed, I recommend use [Opencore Configurator](https://mackie100projects.altervista.org/download-opencore-configurator/) to modify serial number/UUID.

Test laptop specification:
```
- Name: Dell InspIron 13 7370
- Processor: Intel Core i7 8550U
- Wifi: Intel® Dual Band Wireless-AC 7265
- Audio: Realtek Audio
- Graphics: 
  * IGP: Intel UHD Graphics 620
- Display: Build in @1920 x 1080 pixels @60 Hz
- Storage:
  * SSD: ZHITAI TiPlus7100 2TB(Replaced, original SSD it's supported.)
- Dual Boot:
  * Windows 11 Pro 24H2
  * MacOS 15.2 Sequoia
```

[Download EFI on releases](https://github.com/DuolaD/Dell_InspIron_13-7370_OC_EFI/releases/latest)

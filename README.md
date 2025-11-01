# Revive your Nokia N95 ![Nokia](https://img.shields.io/badge/Nokia-%23124191.svg?style=for-the-badge&logo=nokia&logoColor=white)

Revive your old S60v3 FP1 Symbian Nokia N95 (RM-159/RM-160/RM-320) with this guide from _~~2021~~_ 2024!

[![Read in English](https://img.shields.io/badge/Read%20in-English-red)](README.md)
[![Leer en Español](https://img.shields.io/badge/Leer%20en-Español-yellow)](README.es.md)


![Nokia N95](https://user-images.githubusercontent.com/27629528/111556514-1a841600-878b-11eb-8063-5d8cac57c0eb.jpg)

> Both the phone in the photo, as well as the base of this repository, are attributed to [@domib97](https://github.com/domib97)

### **_Description:_**

This repository contains a detailed guide on how to revive your Nokia N95. The main objective is to provide a step-by-step guide to update the firmware, install essential applications and tools, and finally, hack the Symbian S60 operating system to avoid signature errors. <br>
I also want to keep the N95 community alive, so I will use this place to share applications, tools, and useful resources, not only for application development but also for daily use of the phone and enjoyment of it.<br>
Contributions are welcome!

> [!WARNING]
> I cannot guarantee that the links provided in this repository will always be available (they are already quite old). In any case, I will try to ensure that the essential components, both for flashing the firmware and for hacking the operating system, are attached to the repository.

### **_Links:_**

Documentation and reading:
- https://en.wikipedia.org/wiki/Nokia_N95 (wiki)
- https://en.wikipedia.org/wiki/S60_(software_platform) (wiki)
- http://www.allaboutsymbian.com/ (news/forum)

Development:
- https://mrrosset.github.io/Symbian-Archive/index.html (SDKs)
- https://www.mediafire.com/folder/79jhy594xb3uk/Symbian_Development#79jhy594xb3uk (symbian dev tools)

Community:
- https://www.gsmarena.com/nokia_n95-1716.php (still active community)
- https://www.reddit.com/r/symbian/ (Symbian community)
- https://www.reddit.com/r/ngage/ (N-Gage community)
- https://t.me/SymbianElite (Symbian community channel)

Apps:
- http://www.freeware-symbian.com (apps)
- https://de.phoneky.com/applications/?v=0#gsc.tab=0 (apps)
- https://archive.org/download/symbian-games (games)
- https://archive.org/details/nokia-n-gage-the-force-unleashed-2008 (games)

Others:
- http://m.opera.com/?region&act=lp&tag=mini5s60&vid=0x9c7f9c859a2dd90a&cert=all&ua=NokiaN95 (Opera Mini)
- https://s2putty.sourceforge.net/ (PuTTY)
  
### **_Firmware:_**

The latest firmware versions for the Nokia N95 are:
- N95-1 (RM-159) : 35.0.002 ([link](https://www.frendx.com/firmware/download-nokia-n95-rm-159-v35-0-002-stock-firmware-flash-file/))
- N95-2 8GB (RM-320): 35.0.001 ([link](https://www.frendx.com/firmware/download-nokia-n95-rm-320-v35-0-001-stock-firmware-flash-file/))
- N95-3 (RM-160): 35.2.001 ([link](https://www.frendx.com/firmware/download-nokia-n95-3-rm-160-v35-2-001-stock-firmware-flash-file/))
- N95-4 8GB (RM-421) 35.2.002 ([link](https://www.frendx.com/firmware/download-nokia-n95-rm-421-v20-2-005-stock-firmware-flash-file/))

> [!CAUTION]
> Make sure your phone's code matches the firmware you are trying to install. You can find the product code on the back, under the battery, or with the phone itself, by dialing `*#0000#`. <br> If the download links do not work, you can search Google for the firmware corresponding to your model.

### **_Prerequisites:_**

- Nokia N95 (RM-159/RM-160/RM-320 were the models in which I found reports of success)
- Mini-USB cable or computer with Bluetooth connection (To send files to the phone)
- Phoenix Service Software ([link](https://archive.org/download/phoenix_service_software))
- Nemesis Service Suite ([link](https://archive.org/details/nemesis-service-nss))
- A computer with Windows XP/7/8/10/11

### **_Steps to flash the latest firmware:_**

> [!NOTE]
> I flashed the firmware with a Nokia N95-3 (RM-160) on Windows 7. The process may be similar with other models, but I can't guarantee it. It's trial and error. Just in case, I attach [here](https://www.youtube.com/watch?v=BOEaSA_fgTw&t=213s) a video by [@Retrophonesstuff](https://www.youtube.com/@Retrophonesstuff) that details the same process (similar) but with a Nokia N95-2 8GB (RM-320).

1. If you have important information, back it up with Nokia Suite. The installer is located at `/dev/Nokia_Suite_webinstaller_ALL.exe`. Flashing the firmware will erase all the content on the phone.
2. Download Phoenix Service Software, **pause the real-time protection of your antivirus**, unzip it (Password: 1234) and install it.
3. Connect your Nokia N95 to the computer via USB cable (PC Suite Mode) and select the corresponding COM port in "Connections".
4. In File -> Open Product, select your phone model (RM-159, RM-160, or RM-320).
5. Place the downloaded firmware in the folder `C:\Program Files (x86)\Nokia\Phoenix\Products\RM-159` (or the folder corresponding to your model).
6. In Flashing -> Firmware Update, select the firmware and click "Update Software".

> [!NOTE]
> Notes on flashing (Step 6):
> - If Phoenix fails to detect the phone, try another USB cable or USB port, or install the Nokia Connectivity Cable Drivers (located at `/dev/sdk/Connectivity_Cable_Driver.exe`).
> - If you encounter a blue screen of death while trying to recognize the device during the process ([literally](/images/bsod.jpg)) due to Kernel security checks with ADL loading mode, try using a computer with Windows 7, or an older version of Windows 10. In my case, I couldn't flash the phone with Windows 10 or 11, but I could with Windows 7 (Note: in W7 I had to install Nokia Suite, Nokia Connectivity Cable Drivers, and cancel driver review via Windows Update, in that order).
> - If you encounter any errors during flashing, and none of the above works, you can try editing the phone's product code with Nemesis Service Suite (NSS). In `/docs` I attach some useful codes, although you can find them on the internet. **Use NSS with caution! Only change the product code, and make sure the new one is compatible with your model** ([sample image](/images/nss.png)).


### **_Steps to hack S60 Symbian V3:_**

To avoid signature errors and be able to install unsigned applications, it is necessary to hack the operating system.

> [!WARNING]
> Not all hacking methods work for all Nokia N95 models, nor for all firmware versions, so I will detail several methods you can try:


#### **_Method 1 (Norton Hack):_**

**Video tutorial**: [link](https://www.youtube.com/watch?v=rttethei6xg)<br>
Credits to [@tsle805](https://www.youtube.com/@tsle805)

1. Download the necessary files from `/norton_hack` and copy them to your phone via USB/Bluetooth.
2. Change the phone date to 2009.
3. Install `NortonSymbianHack.sisx`.
4. Open Norton -> Options -> Antivirus -> Quarantine -> Restore All.
5. Install `RomPatcherPlus_3.1.sisx`.
6. Open RomPatcher -> Check both options.
7. Remove Norton from the Application Manager.
8. Restore the phone date.

#### **_Method 2 (Mobile Security Hack):_**

**Video tutorial**: [link](https://www.youtube.com/watch?v=UJJICzbk3TA)<br>
Credits to [@Mr_symbian](https://www.youtube.com/@Mr_symbian)

1. Perform a hard reset on the phone (optional) by dialing `*#7370#` (Code: 12345).
2. On the phone (Settings > Applications > App. Manager), make sure the "Software Installation" section is set to "All".
3. Change the phone date to 01/01/2012.
4. Download the necessary files from `/mobile_security_hack` and copy them to your phone via USB/Bluetooth.
5. Install `x-plore v1.30.sisx`.
6. Open X-Plore and navigate to the folder where you copied the files (Files).
7. Open tmquarantine.zip and extract the tmquarantine folder to `C:\`.
8. Install `mobile-security.sisx`. When prompted to restart, do not do it.
9. Open mobile-security, select "Yes" to the first message.
10. Select Options -> Antivirus -> Quarantine list -> Options -> Mark -> Mark all -> Options -> Restore -> Yes.
11. Open X-Plore and navigate to the folder where you copied the files (Files).
12. Install `RomPatcherPlus_3.1_LiteVersion.sisx` or an alternative version if that one doesn't work.
13. Open RomPatcher -> Check both options.
14. Open X-Plore, Tools -> Configuration -> Check all 4 options; "Show hidden files", "Show ROM drives", "Show RAM drives" and "Show system files/folders".
15. Open the Hacker69 folder and choose the folder according to your phone model.
16. Copy the `installserver.exe` file to `C:\sys\bin`.
17. Remove Mobile Security from the Application Manager.

#### **_Alternatives:_**

If the previous methods do not work, you can try an application to "sign" applications. They didn't work for me, but I left the files in `/signing_apps` in case you want to try them.

### **_Development:_**

If you are interested in developing applications for Symbian S60v3, you can find the SDKs in this repository. I also attach some tools and resources that may be useful for development. <br>
You can code with C++ (native), Java ME (native), QT (native) or Python for S60 (PyS60).

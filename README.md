# Fix for "SystemVersion.plist build version mismatch" + "An update is in progress" error in OCLP root patching

I recently struggled but finally managed to fix after trying again and again.
For anyone hitting the "SystemVersion.plist build version mismatch" + "An update is in progress" error in OCLP root patching:

  1	Boot into safe mode (via OpenCore picker: hold Shift + Enter).
	2	Open Terminal and run:

sudo rm -rf /System/Library/AssetsV2/com_apple_MobileAsset_MacSoftwareUpdate/* 
sudo rm -rf  /System/Volumes/Update/* 

3. ⁠Reboot in Safe Mode

4. ⁠Run latest OCLP → Post-Install Root Patch → Apply as usual.
   
5.- Run OCPL-Plus completely and the patch will be applied correctly. Once restarted, the system will be fully functional.

<img width="428" height="591" alt="Captura de pantalla 2026-04-27 a las 12 35 31" src="https://github.com/user-attachments/assets/601a1641-d427-421b-8c1b-bb331e456165" />

  ⁃	SystemVersion.plist build version mismatch: found 12.6
(21G115), expected 26.4.1 (25E253)

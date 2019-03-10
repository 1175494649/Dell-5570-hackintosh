# Dell-5570-hackintosh
MacOs High Sierra and Mojave on Dell 5570



Specs : Dell inspiron 5570 (Inspiron 15 5000series) , with :
Cpu : intel i5-8250u at 1.6ghz (Kabylake-r)
Gpu : Intel uhd620
Ram : 8gb ddr4 2400ghz
Hard disk : I replaced the standard hd with a Samsung 860 evo and I added a Samsung 860evo at m2 slot
Wifi/bt : Factory qualcomm won't work. I replaced it with a Broadcomm 94352z card
Fingerpring sensor : Won't work with mac, so I disabled it.
Card reader : I don't need it , so I disabled it from bios.

What is working : Pretty much everything...
CPU management : native cpu management at High Sierra (see note 1) and Mojave with smbios 15,2.
Battery managment : getting 4,5-5 hours , with browsing , music and office editing. Better that windows 10 !!!
Audio : working great including headphones.
Sleep/wake : lid close / open working as it should . Laptop sleeps overnight with 3-4% battery lost.
Precision touchpad : working close to a real mac , with almost all gestures (see note 4).
Brighness / volume control : fn + F1,F2,F3,F4 for volume , fn+F11,F12 for display brighness.
Camera : ok


What we need :
I will not get into details. You can read the great guides at forum for getting a usb installer for HS or Mojave. Just make sure to replace clover with attached one.

Some notes :

1) If you want to use smbios 15,2 (which I find better for our laptop) you should use Mojave or High Sierra at least on version G65. If you try to install lower High Sierra version you won't be able to boot. If you prefer you can use smbios 14,1 whick will work on all version of HS , but without proper cpu management.

2) With smbios 15,2 be sure to have in your clover/kexts/other folder the notouchid.kext. Otherwise you will be experiencing a lag when prompting for security password.

3) Dispaly analysis is set to 1920x1080 (default). If you find (like me) that fonts are too small you can use a scaled one (like 1600x900). Or you can run one-key-hidpi-masterto get HDIPI , too.

3) You have to implement proper usb management, following this guide :guide-creating-a-custom-ssdt-for-usbinjectall-kext.211311. This is very importart!!! I've already placed a ssdt for usb in the clover/patched , but be sure to check if it is working ok for your system , too. As I said I've disabled card reader and fingerprint sensor , as they don't work on hackintosh.

4) Uncheck smart zoom at preferences/trackpad.

5) Install codecommander.kext at l/e with proper permissions.

6) I have all kexts on clover/other , except codeccommander.kext. You will probably, as Reahabman suggests, want to install them on l/e.

7) Get yourself a serial number in config.plist/smbios.



UPDATE 9/3/19

compatible with High Sierra and Mjojave latest beta

updated kexts to latest verion

updated clover to latest version

improved acpi hotpatch as on real mac

removed ssdt-pnlf , added intelbacklight as per whatevergreen guide

Patch intel uh620 for hdmi audio

Unchecked plygintype so working without HWP. Battery percentage is now accurate (before it was 5-6%off compared to cocounut battery and bios). CPU management and battery consumption seems the same. If you prefer you can enable it again.

notes :
latest voodooi2c kexts not working well. Using a modified version.


Working hard to keep this project alive and up to date. If you feel like it you can buy me a beer :
https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=AUQFM3DPPEEEC&source=url


Please , comment about how's this working for your system. There is room for perfection, with your help.

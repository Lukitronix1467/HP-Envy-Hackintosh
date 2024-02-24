# I'm going to show you how to do a Hackintosh
I've done mine in an HP Envy but scroll down to learn how to do your own. I can do it for you, see the bottom for more info. If you like it, you can buy me a Porsche 911 GT3-RS
## HP-Envy-Hackintosh
Succesfull Hackintosh on a HP Envy Laptop model: 17-cg0000ns

## EFI file

The EFI file contains all you need for a clean installation, all drivers, ACPI, kexts are there. After installations all works fine and how should work on a Hackintosh.

### Features

- Clean installation
- Keyboard support
- video, and resolution support
- USB ports 3.0 ; 2.1 ; 2.0 ; and type-C works
- Bluetooth and Wifi support

Airdrop doesn't work but it appears. You can choose between 2 kexts for Wifi, one is Heliport which uses the ethernet port (USB-C) as wifi. It's more stable but MacOS doesn't recognise it like Wifi so you don't have airdrop option or Airplay. With the other, which is twline, you can use wifi as the wifi option on MacOS and the ethernet too. With this option you have Airplay working and other wireless services that MacOS offers.

> Sorry for the English, I'm not English fluent, I'm Spanish.


### Issues

I have some post-installation issues that I'm trying to solve.

- Speakers Issue (Speakers don´t work, I use Airpods)
- Jack port Issue (Jack port doesn't work, I don't use it anyway)
- Trackpad Issue (Doesn't recognize Trackpad, I use the magic mouse (Normal mouse is also available) )

The battery is working for me, keyboard keys... All works fine.

## Installation
### Preparatives
Here, I'm going to explain how to do your hackintosh. First, you need to know if you are going to do it via MacOS, Linux or Windows. Now, you need to choose your target computer. It can be either a laptop or a desktop PC. Now, I only tried with Intel processors so if you have AMD, I'm sorry. You need to know what Intel processor you have, help yourself from this table:

| Processor | Code Name |
| ------ | ------ |
| Intel 2ndth gen Core i-series | Sandy Bridge |
| Intel 3rd gen Core i-series | Ivy Bridge |
| Intel 4th gen Core i-series | Haswell |
| Intel 5th gen Core i-series | Broadwell |
| Intel 6th gen Core i-series | Skylake |
| Intel 7th & 8th gen Core i-series | Kaby Lake & Kaby Lake R|
| Intel 10th gen Core i-series | Ice Lake |
| Intel 11th gen Core i-series | Tiger Lake |
If you don't know which is your Processor, you can search on these webs:
> [Intel CPU generation list](https://www.pcguide.com/cpu/intel-cpu-generation-list/)
> [How to find the code name for Intel Processors](https://www.intel.com/content/www/us/en/support/articles/000027640/processors.html)


#### Get to know your computer components

Things you will need for your MacOS:
- GPU (Graphics)
- Your storage devices (HDD/SSD, NVMe/AHCI/RAID/IDE configuration)
- Your laptop/desktop model if from an OEM
- Your Ethernet chipset
- Your WLAN/Bluetooth chipset

Almost there, now that we have all we need I'm going to let you choose between two methods of doing your EFI file.

> 1 Create your own EFI file from Scratch (If you choose this option, [read OpenCore Guide](https://dortania.github.io/OpenCore-Install-Guide)) <--- Warning! You need to have code experience and a lot a lot a lot of patience
> 2 Take an EFI file already made for your processor (If you choose this option, continue scrolling)

### Software
| App Name | Link | Alternative Link (For Mac users)
| ------ | ------ | ----- |
| Etcher Balena | https://etcher.balena.io |
| Gen SMBIOS | https://github.com/corpnewt/GenSMBIOS |
| Proper Tree | https://github.com/corpnewt/ProperTree |
| Explorer ++ | https://explorerplusplus.com | https://www.olarila.com/files/Utils/ESP%20Mounter%20Pro.app_v1.9.1.zip |
| MacOS ISO | [/MacOS-ISO/](https://www.olarila.com/topic/6278-olarila-vanilla-images-macos-installer/) |
| EFI file | https://www.olarila.com/topic/25111-hackintosh-efi-folders-with-opencore-mod/ |

You need to have a 32Gb Hard Drive.
## Getting Started
### From MacOS
The first thing we need to do is take our Hard Drive and plug it into our Mac. Now we open [Etcher Balena](https://etcher.balena.io) Choose your MacOS ISO and follow the instructions.

![Alt text](https://etcher.balena.io/images/Etcher_steps.gif "Etcher Balena Preview")

While it's flashing, we can now create our Mac serial. This is what tells to Apple that our "Mac" is a legit Mac and we get access to AppStore, Apple Music, iMessage, iCloud...

To do this, we need to run [Gen SMBIOS](https://github.com/corpnewt/GenSMBIOS) by right-clicking the .command file and clicking open. A terminal window will appear.

![Alt text](https://user-images.githubusercontent.com/13791385/139742414-c20303de-e77a-45ac-8fd2-d2b4908f8979.png "Gen SMBIOS Preview")

> First, press 1 to install/ Update
> Now, press 2 and drag your config.plist that is in your EFI folder in OC (EFI/OC)
> Now, press 3 to Generate SMBIOS.
> Lastly, press Q to quit.

After Etcher Balena is Finished, you need to partition your Drive. Open [ESP Mounter Pro](https://www.olarila.com/files/Utils/ESP%20Mounter%20Pro.app_v1.9.1.zip) and an icon will appear in your menu bar:

![Alt text](https://i0.wp.com/manjaro.site/wp-content/uploads/2022/03/Screen-Shot-2022-03-02-at-10.51.39.png?resize=768%2C366&ssl=1 "ESP Mounter Pro Preview")

You can now see your Hard Drive. Now you click on mount and an EFI Hard Drive Partition will appear. If there's any folder, erase it and paste your EFI folder in it. Now you can unmount it. Eject the Drive and turn off your target computer. Now you are ready for:

### Running it
Plug your Hard Drive on your computer and start it while spamming either F2, F9, F10 or F12 (It depends on your computer). Now you should see the BIOS. Boot your computer with the hard drive and you should see this: (Ignore the text, just focus on the three icons that should be similar)

![Alt text](https://i.ytimg.com/vi/qxZ_oZ9Qrtc/maxresdefault.jpg "Preview")

Now, with arrow keys go to the Recovery Option. Now, click on Disk Utilities and erase your computer's Hard Disk. Then quit the app and hit install MacOS "Your version". Select the Hard Drive you just erased and follow the instructions.

### From Windows

Follow the MacOS guide but instead of using the ESP Mounter Pro use Explorer++. Instead of executing the .command files, execute .bat. Follow this tutorial for Windows that explains with images:

https://www.youtube.com/watch?v=kwbOf-dDtpc

## Post Installation Issues

[Click Here to see the post-installation issues and how to fix them](https://dortania.github.io/OpenCore-Post-Install/#how-to-follow-this-guide)

## Troubble Shoutting

[Click Here to see the post Troubble Shoutting issues and how to fix them](https://dortania.github.io/OpenCore-Install-Guide/troubleshooting/troubleshooting.html)

## Finish

That's it, the end of the Tutorial, hope you liked it and if you want me to do it for you, just send me all your computer info and I'll do it.

mail: disco-dole-0n@icloud.com

Buy me a Porsche 911 GT3-RS: https://www.paypal.com/donate/?hosted_button_id=ETTK7H8X4PTSJ
## License
Lukitronix1467

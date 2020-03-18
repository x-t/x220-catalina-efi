# x220-catalina-efi

Prev. - [Mojave (info)](https://github.com/x-t/x220-mojave-efi), [guide](https://github.com/b-ggs/x220-hackintosh)

Last version without dosdude1 patches - [High Sierra](http://x220.mcdonnelltech.com/) (anything that runs on a 2011 MBP)

Last version (reportedly) without graphical glitches - [Sierra](http://x220.mcdonnelltech.com/macos-sierra-installation/)

It can be used as a daily driver now, although Mojave will probably be more stable in the long run, as you wouldn't have to update it.

This repo is more for research than a guide, I cannot be bothered to make a guide, there are countless examples of them everywhere. There aren't many massive changes from Mojave to Catalina to warrant a new tutorial.

Current status - it works as well as before

There are some things I don't bother to test because I don't use/have the things
* Bluetooth
* Webcam

## Tools

* dosdude1's Catalina patcher [link](http://dosdude1.com/catalina/)
* Clover Configurator [link](https://mackie100projects.altervista.org/download-clover-configurator/)
* Clover r5070

## Regular issues not fixed by upgrading to Catalina

* Graphical glitches
* Microphone volume is ignored and is stuck on 100%, ear raping everyone that has to listen to it

## Installation changes from Mojave

* The installer will tell you that the post-install tool is launched during the install, this isn't enough. After you reboot from the installer, go back to the installer and patch up everything, make sure that you check "force cache rebuild".
* `drivers64` has been deprecated and you have to use `drivers` now, good thing you can just copy stuff from `drivers64UEFI` to `drivers/UEFI`

## General knowledge

* When modifying config.plist, uncheck FixUSB, FixDisplay, and FixIntelGFX. If you don't do that, you won't be able to boot back anymore.
* iMessage will not work no matter how hard you try.
* App Store works without serial number changes.
* You will have to generate a new serial number to use iCloud.

## Screenshot

![Desktop](https://i.arxius.io/0098daee.png)

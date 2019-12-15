# x220-catalina-efi

This is a work in progress, don't try to do shit if you don't know what you're doing.

~~In no way, shape or form is this daily driver material. Use Mojave instead, it's way more stable. [x-t/x220-mojave-efi](https://github.com/x-t/x220-mojave-efi)~~

It can be used as a daily driver now, although Mojave will probably be more stable.

This repo is more for research than a guide, I cannot be bothered to make a guide, there are countless examples of them everywhere. There aren't many massive changes from Mojave to Catalina to warrant a new tutorial.

Current status - ~~fuckin borked lmao~~ ~~tested, has issues.~~ tested once more, still has some issues

There are some things I don't bother to test because I don't use/have the things
* Bluetooth
* Webcam

## Tools

* dosdude1's Catalina patcher [link](http://dosdude1.com/catalina/)
* Clover Configurator [link](https://mackie100projects.altervista.org/download-clover-configurator/)
* Clover r5070

## *Solved* Issue - Audio

It has been solved. Make sure to boot back into the installer and launch Post-install patcher, select "force cache rebuild" and it should be fixed. Lilu/AppleALC work fine too.

~~*This part is outdated, at this point you most likely have audio working. Follow issue #1. I just don't have the time to try myself. [Link to kexts](https://github.com/x-t/x220-catalina-efi/files/3701053/Kexts.zip).*~~

~~Audio doesn't work, at all. Tried `AppleHDA_20672.kext` and [AppleALC](https://github.com/acidanthera/AppleALC) with [Lilu](https://github.com/acidanthera/Lilu), neither can output any audio.~~

~~Audio does seem to work under some circumstances ([#1](https://github.com/x-t/x220-catalina-efi/issues/1)), but personally I haven't had luck with it.~~

## *Solved?* Observation - Display brightness

Brightness seems to be messed up in Catalina, with it being almost 5 notches brighter in Mojave or High Sierra. ~~I don't remember a difference with/without `AppleBacklightInjector.kext`~~

Currently you have two options:
* Install `AppleBacklightInjector.kext` and have 100% brightness without the ability to turn it down
* Don't install `AppleBacklightInjector.kext` and have a range of 0-60% brightness

After putting my laptop to sleep and waking it back up again, all brightness options are back (`AppleBacklightInjector.kext` not installed)

## Regular issues not fixed by upgrading to Catalina

* Graphical glitches
* Microphone volume is ignored and is stuck on 100%, ear raping everyone that has to listen to it

## Installation changes from Mojave

* ~~No need to boot back into the installer to run the post-install tool, the patches are applied during the install.~~ They don't apply fully, so you still have to do that.
* `drivers64` has been deprecated and you have to use `drivers` now, good thing you can just copy stuff from `drivers64UEFI` to `drivers/UEFI`

## Screenshot

![Desktop](https://i.arxius.io/0098daee.png)

## General knowledge

* When modifying config.plist, uncheck FixUSB, FixDisplay, and FixIntelGFX. If you don't do that, you won't be able to boot back anymore.
* iMessage will not work no matter how hard you try.
* App Store works without serial number changes.
* You will have to generate a new serial number to use iCloud.

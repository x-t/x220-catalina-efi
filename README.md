# x220-catalina-efi

This is a work in progress, don't try to do shit if you don't know what you're doing.

In no way, shape or form is this daily driver material. Use Mojave instead, it's way more stable. [x-t/x220-mojave-efi](https://github.com/x-t/x220-mojave-efi)

This repo is more for research than a guide, I cannot be bothered to make a guide, there are countless examples of them everywhere. There aren't many massive changes from Mojave to Catalina to warrant a new tutorial.

Current status - ~~fuckin borked lmao~~ tested, has issues.

There are some things I don't bother to test because I don't use/have the things
* Bluetooth
* iCloud, iMessage, etc. [1]
* Webcam

## Tools

* dosdude1's Catalina patcher [link](http://dosdude1.com/catalina/)
* Clover Configurator [link](https://mackie100projects.altervista.org/download-clover-configurator/)
* Clover r5070

## Issue - Audio

Audio doesn't work, at all. Tried `AppleHDA_20672.kext` and [AppleALC](https://github.com/acidanthera/AppleALC) with [Lilu](https://github.com/acidanthera/Lilu), neither can output any audio.

![No output devices](https://i.arxius.io/62337b3b.png)

## Installation changes from Mojave

* No need to boot back into the installer to run the post-install tool, the patches are applied during the install.
* `drivers64` has been deprecated and you have to use `drivers` now, good thing you can just copy stuff from `drivers64UEFI` to `drivers/UEFI`

## Screenshot

![Desktop](https://i.arxius.io/99c49b7b.png)

### Footnotes

[1]: App Store works, if you changed the serial number Apple ID and its services should start working, I've never done that, because when I do my computer stops booting.

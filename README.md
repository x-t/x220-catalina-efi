# x220-catalina-efi

This is a work in progress, don't try to do shit if you don't know what you're doing.

In no way, shape or form is this daily driver material. Use Mojave instead, it's way more stable. [x-t/x220-mojave-efi](https://github.com/x-t/x220-mojave-efi)

Current status - tested, has issues.

## Tools

* dosdude1's Catalina patcher [link](http://dosdude1.com/catalina/)
* Clover Configurator [link](https://mackie100projects.altervista.org/download-clover-configurator/)
* Clover r5070

## Audio

Audio doesn't work, at all. Tried `AppleHDA_20672.kext` and [AppleALC](https://github.com/acidanthera/AppleALC) with [Lilu](https://github.com/acidanthera/Lilu), neither can output any audio.

![No output devices](https://i.arxius.io/62337b3b.png)

## Installation changes from Mojave

No need to boot back into the installer to run the post-install tool, the patches are applied during the install.

## Screenshot

![Desktop](https://i.arxius.io/99c49b7b.png)

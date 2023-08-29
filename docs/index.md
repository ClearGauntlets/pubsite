# Welcome to ClearWiki! 

<p align="center">
<img src="https://avatars.githubusercontent.com/u/114621125?s=200&v=4"/>
</p>

This website is the home of the ClearGauntlets project, a fork of the LucidVR project focusing on refining the "reel" design of Prototype 4.1 to create a sleeker, more effective virtual reality glove. The main gimmick of this project is "premium" design. The price ceiling per pair is raised from $60 to $200, but for that, we hope to give you simpler, smaller, more reliable reels, a better PCB and wiring harness, and SteamVR tracking!

Please bear with us as we build all this, it's really complicated.

This website also hopes to become a resource for anyone looking to get into VR hacking, a starting place for learning the basic components of a VR system, a host for detailed descriptions, source code, schematics, and guides. Ideally, you will be able to go from zero to full pair of custom gloves just by clicking through this website.

Find the rest of our stuff at <https://github.com/cleargauntlets>
# Projects

ClearGauntlets is composed of a handful of projects designed to produce a premium, DIY-friendly pair of haptic feedback gloves. The project is essentially a glorified fork of the LucidVR project, and tries to maintain as much upstream compatibility as possible, with any deviations well-documented.

## [CG Proto 2](https://cad.onshape.com/documents/c8017346b70c8e3a1c702b01/v/0d6c6a28e6c30c029db12761/e/4ca1df952223ccb607a2af60?renderMode=0&uiState=64541595e88e363a59e62839)
Our re-design of LucidGloves Proto 4. The above link contains a read-only Onshape workspace. If you just want the STLs, [click here](https://github.com/ClearGauntlets/STL/blob/v2.0/ClearGauntletsSTLs.zip)

## [PCB](https://github.com/ClearGauntlets/ClearGauntlet-PCB)
A compact PCB designed to break out all the IO you'll need in an extremely tight package.

## [Power](https://github.com/ClearGauntlets/Power)
The power module used to drive the ESP32 and Servos (and, perhaps one day, a custom tracker)
**This doesn't exist yet. Hopefully it will soon.**

## [Firmware](https://github.com/ClearGauntlets/lucidgloves/tree/main/firmware/lucidgloves-firmware)
A fork of the [LucidGloves](https://github.com/LucidVR/lucidgloves) project that we base our firmware off of.

## [UI](https://github.com/ClearGauntlets/opengloves-ui)
A fork of LucidVR's UI system.

## [Driver](https://github.com/ClearGauntlets/opengloves-driver)
Our Fork of the LucidVR Steam Windows Drivers

## [Tracker](https://github.com/ClearGauntlets/vive-diy-position-sensor)
A custom implementation of a Lighthouse V1 tracker. This is an extremely cheap way to enable tracking for your project.

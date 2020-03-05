MRFIXIT RECALBOX RELEASES FOR ROCKCHIP BOARDS


This repository contains the most up-to-date downloads for all Recalbox releases by MrFixIt. These are community builds that have been in development for some time now and have included a good number of contributors in both testing as well as debugging. The majority of these contributors are from the PINE64 community (http://www.pine64.org), who I continue to be impressed by.

-- The download is located under this repository's releases -- https://github.com/mrfixit2001/recalbox-rockchip/releases


MrFixIt's custom kernel and u-boot sources are based on the Rockchip BSP Kernel but have a large number of additional fixes, customizations, and back-ports. Sources are here:
* MrFixIt Kernel: https://github.com/mrfixit2001/rockchip-kernel
* MrFixIt U-Boot: https://github.com/mrfixit2001/rockchip-u-boot

For those of you unfamiliar with Recalbox: https://www.recalbox.com/ "Recalbox offers a wide selection of consoles and game systems. From the very first arcade systems to the NES, the MEGADRIVE, 32-bit platforms (such as the Playstation) and even Nintendo64. With Kodi already included, Recalbox also serves as a Media Center. By connecting it to your home network, you will be able to stream videos from any compatible devices (NAS, PC, External HDD, etc.)."


Recalbox's source is available on their main repo: https://gitlab.com/recalbox


I submitted the changes to support the Rockchip port in the recalbox master repo in September 2019 but at the time of writing this it has yet to be merged. That source can be found here: https://gitlab.com/recalbox/recalbox/-/merge_requests/840


When reporting issues:

* Provide logs and/or screenshots of the issue so that we can see the error(s) you are seeing
* Provide detailed steps for us to follow in order to reproduce the issue


We STRONGLY recommend that you install a heatsink on the board CPU intensive tasks, such as 4K playback and demanding emulators, can create a substantial amount of heat. You can monitor your board's temperature and stats by enter it's IP address in a browser.


The Rockchip port has some additions and features that are exclusive to the MrFixIt releases:
* Kodi updated to 18.5 Leia and patched to support CEC and 4K HDR Playback
* Restart Bluetooth Option
* Suspend (where supported)
* Updated emulator core versions
* Additional emulator cores added
* Default configs optimized for each Rockchip board
* Included support for the Roshambo Case (https://www.cloudmedia.com/?product=roshambo-retro-gaming-case)
* Wolfenstein 3D (Shareware version) included in DosBox
* Overclock options (only for RK3328 at this time)


A few things to know about this release: 
* When the image first boots, you can expect a delay as the partition is expanded to the full size of your disk. Please be patient and let this complete. It will not happen on every boot, but you should not interrupt this process or you may need to reimage.
* N64 has multiple core options, different ROMS work better with different cores! So if your game isn't running well, try another core! So far even the most demanding games have been found to run perfectly with the right core selected.
* Some emulators / cores are highly dependent on a valid BIOS files being installed (Dreamcast, for example). Be sure to read the documents in the system’s ROM folder for details on what BIOS files are needed. Further documentation is available on the Recalbox wiki.
* A single ROM not working is not considered a "bug", it's often an incompatibility with the ROM and the emulator / core. We have provided multiple cores for some emulators to try and help maximize the number of ROMS that work.


Important Note about Widescreens: The majority of users will be using widescreen monitors and TVs with 16:9 aspect ratios these days, and most of these will automatically stretch a 4:3 video to 16:9 to make it full screen. This distorts the graphics and makes everything look stretched out and askew. So, I have added custom patches and new configuration settings to Mupen64, Reicast, and Retroarch to correct this so that the emulators will still render at the right scale after being stretched. :) This is ON by default. If you do not have a widescreen monitor, or your monitor does not have this auto-stretch feature, then your games may not be centered or look too thin. In this case, simply make the following one-time changes to the configurations to turn off these customizations:
* Retroarch: use the retroarch menu to change the default - Settings->Video->Aspect Ratio
* Reicast: change the setting "rend.FixAspect" to 0 in /recalbox/share/system/configs/reicast/emu.cfg
* Mupen64: each video plugin (core) has been given it's own setting, allowing you to customize each to your own needs, and GLES2N64 (n64 core) has it's own config file. The settings for these plugins are in /recalbox/share/system/configs/mupen64 in the files mupen64plus.cfg and gles2n64.conf. Just change the listed widths and left offsets to whatever your needs are.


Lastly, please remember this is a community build, and just something I've worked on in my free time. There's no pressure at all, but if you appreciate the work then feel free to buy me a virtual beer on Paypal: mrfixit2001 at gmail.

Special thanks go out to the LibreELEC and Recalbox teams, as well as LukasZ at Pine64 for his huge efforts in research, testing, and feedback!

Mr Fix-IT

<p align="center">
<img src="https://github.com/Colt-Enigma/platform_manifest/blob/c12/assets/Banner_1.png" > 
</p>

ColtOS Android-12.1
===============================

[![Download ColtOS](https://img.shields.io/sourceforge/dm/coltos.svg?color=3498DB&label=ColtOS%20Downloads&style=for-the-badge&labelColor=1B4F72&logo=sourceforge)](https://sourceforge.net/projects/coltos/files)
[![Download ColtOS](https://img.shields.io/sourceforge/dw/coltos.svg?color=3498DB&label=ColtOS%20Downloads&style=for-the-badge&labelColor=1B4F72&logo=sourceforge)](https://sourceforge.net/projects/coltos/files)
[![TG chat](https://img.shields.io/badge/Support-Telegram-%233498DB.svg?style=for-the-badge&logo=telegram&&labelColor=1B4F72)](https://t.me/ColtEnigma)

How to Build?
-------------
### Getting the source
- Making required directories
- Obtaining the repo binary
- Adding repo binary to your path
- Giving the repo binary proper permissions
- Initializing an empty repo
- Syncing the repo

Alright, so now we’re getting there. I have outlined the basics of what we’re about to do and broke them down as I know them. This is all pretty much going to be copy/paste so it’ll be fairly difficult to screw this up :)

##### Make directory for the repo binary

      $ mkdir ~/bin

##### Add directory for the repo binary to its path

      $ PATH=~/bin:$PATH

##### Downloading repo binary and placing it in the proper directory

      $ curl http://commondatastorage.googleapis.com/git-repo-downloads/repo > ~/bin/repo

##### Giving the repo binary the proper permissions

      $ chmod a+x ~/bin/repo

To initialize your local repository using the ColtOS trees, use a 
command like this:

```bash
  repo init -u https://github.com/Colt-Enigma/platform_manifest -b c12.1
```
  
Then to sync up:
----------------

```bash
repo sync --no-tags --no-clone-bundle --force-sync -c
```
Finally to build:
-----------------

```bash
  First You need to add the following lines in your Device Tree's colt_devicename.mk file

  TARGET_BOOT_ANIMATION_RES := 1080 : Please change as per your device resolution

  # Inherit some common ColtOS stuff.
  $(call inherit-product, vendor/colt/config/common_full_phone.mk)
  COLT_BUILD_MAINTAINER := RakeshBatra
 
  and use the following to build:

  . build/envsetup.sh
  lunch colt_[device-codename]-userdebug
  make colt -j$
```

Help from other devices for making them Official
------------------------------------------------

If you got some commits missing in our sources for your device, let us know on our telegram chat. Everything else, it's up to you at the time of building.

Credits
-------
* [**Nitrogen Project**](https://github.com/nitrogen-project)
* [**LineageOS/Cyanogenmod**](https://github.com/LineageOS)
* [**AospExtended**](https://github.com/AospExtended)
* [**DirtyUnicorns**](https://github.com/DirtyUnicorns)
* [**BlissRoms**](https://github.com/BlissRoms)
* [**ABC ROM**](https://github.com/ezio84)
* [**GZOSP**](https://github.com/GZOSP)
* [**Pure Nexus**](https://github.com/PureNexusProject)
* [**OmniROM**](https://github.com/omnirom/)
* [**AOSPA**](https://github.com/aospa/)
* [**Project-Xtended**](https://github.com/Project-Xtended/)
* [**Project-Legion**](https://github.com/Project-LegionOS/)
* [**Thanks to all the custom rom community**]


Thanks & regards,
-----------------

#TeamColt


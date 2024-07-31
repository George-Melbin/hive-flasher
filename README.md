## Hive OS Drive Flashing Utility

![how it looks like](https://user-images.githubusercontent.com/38013470/45325818-a2ee2400-b55a-11e8-9905-6072a9d904b2.png)


This is a bulk flashing utility which will help you to do 
headless and keyboardless migration to Hive of your farm.

You can find prebuild image here http://download.hiveos.farm/



### Step by Step Usage Instructions

- Download hive-flasher image from http://download.hiveos.farm/
- Download the latest Hive OS image or it will be downloaded automatically on first boot (by default stable version).
- Write hive-flasher.img to your Flash drive with Etcher (https://etcher.io/).
- After writing the image you will find HIVE-INSTALL folder with README.txt and other config files.
- Use the following FARM_HASH to attach rig to your web account



### Flasher Config

There is a file `flasher-config.txt` with some settings of flasher.

`SHUTDOWN_AFTER_FLASHING=1` will shutdown rig after successful image writing.

`FARM_HASH=` go to your account on the web and find FARM_HASH value.

Also as alternative variant? you can put your `rig.conf` into hive-install folder.



### Advanced. Custom flasher system build.

> This is just for fun, you don't have to do this 

You can make flasher image by yourself with the following steps.

- Create Ubuntu Server installation to SSD
- Put these files on disk
- Run `postinst`
- Put the latest Hive image to /mnt/hive-install (you'd better create NTFS partition)
- Put your starting rig id /mnt/hive-install/RIG_ID_SEQUENCE.txt and password into RIG_PASSWD.txt 
- Boot from this SSD on the rig leaving rig's drive in place
- After boot the script will detect rig's drive and hive flash image there with and precreate rig.conf
- ...
- PROFIT


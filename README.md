MultiBoot menu and tools for Odroid C2
===================================================

About
-----

Boot menu for selecting from available OS's<br />
Backup tool for backup operating system(s) from multiboot card or original Odroid card<br />
Universal installer which can install **android**, **linux**, **OpenELEC** or any combinations (**multiboot**) from USB drive.<br />

---

**Multiboot features**

- boot menu for selecting operating system or Multiboot tools
- automaticaly detects installed operating systems on **all** inserted cards (EMMC and/or SD card)
- mimimal changes to original OS images, only fstab is adjusted for multiboot
- on **Odroid C2** both EMMC and SDcard can be inserted and the OS can be booted from EMMC or SDcard


**Installer features**

- **interactive** installer
- user can set desired partition sizes and installation destination (SD or EMMC)
- it is possible install to **SD Card** and to **EMMC**
- supports **multi boot installation** (Android, Linux, OpenELEC)
- tested with latest Linux versions for C2

**Installer usage**

- build the installer sdcard/image running `sudo ./prepare_selfinst <destination_card>|<destination_image_name> c2|xu4`
- if the image file is created, you can write the image to SDCard using dd command.
  - copy your installation sources (Android update image **update.zip**, Linux **.img**, OpenELEC **.tar** file) to the first partition of your USB drive
  - **rename** the Linux installation image to **linux.img** !
  - on Odroid UX4/XU3 set the **boot switch** to boot from SDCard
  - connect you USB drive to Odroid, insert SDCard and power on
  - select Install from menu
  - follow the instructions to select desired partition sizes and installation destination (**SDCard** or **EMMC**)

**HINTS**
- add **#DESCRIPTION my_os_description** line to **boot.ini.[android|linux|oelec]** files to describe your OS in boot menu

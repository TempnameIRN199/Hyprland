### WIFI

`iwctl`
`station list`
`station` *name-adapter* `get-networks`
`station` *name-adapter* `connect` *SSID*
*wait 10-15 sec.* 
`quit`

### Configure Package Manager

`ping google.com`
`nano /etc/pacman.d/mirrorlist`
*if generate > 30, return to first step*
*if generate 30, continue*
`nano /etc/pacman.conf`
`ctrl + w` *n' find -* `ParallelDownloads`
`in ParallelDownloads change value to 15`
`crtl + s` *n'* `ctrl + x`

### Partition the disks

`lsblk`
`cfdisk /dev/`*disk-name*
*select label type* - `gpt`
*choose* `new` *n' enter* `1M`
*-choose* `type` *n' enter* `BIOS Boot`

*now, we have 2 device, choose the second*
*choose* `new` *n' press* `Enter`
*choose* `write` *n' enter* `yes`

### Format the partitions

*quit* `cfdisk`

*currently,* `mkfs.ext4 /dev/`*disk2-name*
*for example,* `mkfs.ext4 /dev/sda2`

### Mount the file systems

`mount /dev/sda2 /mnt`

### Install package

[[Install package]]

### Generate fstab

`gebfstab /mnt`
`genfstab /mnt >> /mnt/etc/fstab`

### Change directory (arch-root)

`arhc-chroot /mnt`

### Enable services

`systemctl enable NetworkManager`
`systemctl enable sddm`

### Create user

`useradd -m` *user-name*
`passwd` *user-name*
`passwd root`

### Give sudo

`nano /etc/sudoers`
`ctrl + w` *n' find -* `root ALL`
*below this line by the* - `*user-name* ALL=(ALL:ALL) ALL`
`crtl + s` *n'* `ctrl + x`

### Locale n' language system

`nano /etc/locale.gen`
`ctrl + w` *n' find -* `en_US.UTF-8`
`ctrl + w` *n' find -* `ru_RU.UTF-8`
`ctrl + w` *n' find -* `uk_UA.UTF-8`
`crtl + s` *n'* `ctrl + x`

`nano /etc/locale.conf`
*enter* `LANG="en_US.UTF-8"`
`locale-gen`

### Download GRUB

`grub-install /dev/sda`
`nano /etc/default/grub`
*in line* `GRUB_CMDLINE_LINUX_DEFAULT="loglevel=3 quiet"` *u'll delete* `quiet`
`crtl + s` *n'* `ctrl + x`
`grub-mkconfig -o /boot/grub/grub.cfg`

### Exit n' reboot
`exit`
`umount /mnt
`reboot`


### Change shell
`chsh`
`/bin/fish`


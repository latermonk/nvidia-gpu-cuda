
#  check system version

******


```
No LSB modules are available.
Distributor ID:	Ubuntu
Description:	Ubuntu 18.04.3 LTS
Release:	18.04
Codename:	bionic

```
##   install gcc

```
apt update 

apt  install build-essential
```


#  disbale nouveau driver

***/etc/modprobe.d/blacklist-nouveau.conf***

```
vim  /etc/modprobe.d/blacklist-nouveau.conf


blacklist nouveau
options nouveau modeset=0


```

# ***Reboot into text mode (runlevel 3)***

```
Reboot into text mode (runlevel 3)



vim /etc/default/grub

GRUB_CMDLINE_LINUX_DEFAULT的值修改为： "text"

update-grub

reboot


```

#  






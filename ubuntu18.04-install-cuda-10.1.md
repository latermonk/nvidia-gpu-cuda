
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
init 3

reboot

init 3

```

#  config env var


```

export PATH=/usr/local/cuda-10.1/bin:$PATH

export LD_LIBRARY_PATH=/usr/local/cuda-10.1/lib64:$LD_LIBRARY_PATH


```







# nvidia-gpu-cuda     

##  Guide   
https://docs.nvidia.com/cuda/cuda-installation-guide-linux/index.html       


##  Download   
https://developer.nvidia.com/cuda-download    
https://developer.nvidia.com/cuda-10.0-download-archive     

下载安装```cuda_10.1.243_418.87.00_linux.run```


##  cuda_10.0.130_410.48_linux.run

```
init 3

vim /usr/lib/modprobe.d/dist-blacklist.conf

Add:

blacklist nouveau


```


```

init 3  


mv /boot/initramfs-$(uname -r).img /boot/initramfs-$(uname -r).img.bak


dracut /boot/initramfs-$(uname -r).img $(uname -r)

reboot


```


```
init 3 

./cuda_10.0.130_410.48_linux.run




```



```
Installing the NVIDIA display driver...
Installing the CUDA Toolkit in /usr/local/cuda-10.0 ...
Missing recommended library: libGLU.so
Missing recommended library: libX11.so
Missing recommended library: libXi.so
Missing recommended library: libXmu.so

Installing the CUDA Samples in /root ...
Copying samples to /root/NVIDIA_CUDA-10.0_Samples now...
Finished copying samples.

===========
= Summary =
===========

Driver:   Installed
Toolkit:  Installed in /usr/local/cuda-10.0
Samples:  Installed in /root, but missing recommended libraries

Please make sure that
 -   PATH includes /usr/local/cuda-10.0/bin
 -   LD_LIBRARY_PATH includes /usr/local/cuda-10.0/lib64, or, add /usr/local/cuda-10.0/lib64 to /etc/ld.so.conf and run ldconfig as root

To uninstall the CUDA Toolkit, run the uninstall script in /usr/local/cuda-10.0/bin
To uninstall the NVIDIA Driver, run nvidia-uninstall

Please see CUDA_Installation_Guide_Linux.pdf in /usr/local/cuda-10.0/doc/pdf for detailed information on setting up CUDA.

Logfile is /tmp/cuda_install_3062.log

```



##  cuda_10.0.130.1_linux.run


##  set env 

```
export PATH=/usr/local/cuda-10.0/bin:$PATH
export LD_LIBRARY_PATH=/usr/local/cuda-10.0/lib64:$LD_LIBRARY_PATH




source ~/.bash_profile

```
##  verify


```


nvidia-smi





```



```

Install docker 19.03:


 yum install docker-ce-19.03.0-3.el7 docker-ce-cli-19.03.0-3.el7 containerd.io
```



----

##  GPU load test        
https://github.com/wilicc/gpu-burn       

http://wili.cc/blog/gpu-burn.html    

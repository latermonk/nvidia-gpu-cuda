# nvidia-gpu-cuda     


##  nvcc -V

```
nvcc: NVIDIA (R) Cuda compiler driver
Copyright (c) 2005-2019 NVIDIA Corporation
Built on Sun_Jul_28_19:07:16_PDT_2019
Cuda compilation tools, release 10.1, V10.1.243

```


####   故障  nvidia-smi 命令失败


```
modprobe nvidia
```



```
step1：sudo apt-get install dkms

step2: sudo dkms install -m nvidia -v 410xxxxxx.xx

```
再次输入nvidia-smi时，你熟悉的界面就会回来啦。


其中step2 中的***410.79***是***NVIDIA的版本号***，当你不知道的时候，进入/usr/src目录中，可以看到里面有***nvidia文件夹***，后缀就是其版本号






##  CUDNN 

https://developer.nvidia.com/rdp/cudnn-archive   




#  RESULT

```
root@i-022D8229:~/Downloads# ./cuda_10.1.243_418.87.00_linux.run 
===========
= Summary =
===========

Driver:   Installed
Toolkit:  Installed in /usr/local/cuda-10.1/
Samples:  Installed in /root/, but missing recommended libraries

Please make sure that
 -   PATH includes /usr/local/cuda-10.1/bin
 -   LD_LIBRARY_PATH includes /usr/local/cuda-10.1/lib64, or, add /usr/local/cuda-10.1/lib64 to /etc/ld.so.conf and run ldconfig as root

To uninstall the CUDA Toolkit, run cuda-uninstaller in /usr/local/cuda-10.1/bin
To uninstall the NVIDIA Driver, run nvidia-uninstall

Please see CUDA_Installation_Guide_Linux.pdf in /usr/local/cuda-10.1/doc/pdf for detailed information on setting up CUDA.
Logfile is /var/log/cuda-installer.log


```

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

```

https://github.com/nvidia/nvidia-container-runtime#docker-engine-setup

Docker Engine setup



```


```
https://tensorflow.google.cn/overview/
```


----

##  GPU load test        
https://github.com/wilicc/gpu-burn       

http://wili.cc/blog/gpu-burn.html    


```
./gpu_burn 120   

```




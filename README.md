# nvidia-gpu-cuda     

##  Guide   
https://docs.nvidia.com/cuda/cuda-installation-guide-linux/index.html       


##  Download   
https://developer.nvidia.com/cuda-download    




```
export PATH=/usr/local/cuda-9.1/bin:$PATH
export LD_LIBRARY_PATH=/usr/local/cuda-9.1/lib64:$LD_LIBRARY_PATH
```

```
export PATH=/usr/local/cuda-10.1/bin:$PATH
export LD_LIBRARY_PATH=/usr/local/cuda-10.1/lib64:$LD_LIBRARY_PATH
```

```
deviceid:xxxx
api-key:xxxxx
去网页授权License。
拿到授权License后，请更新相应的配置文件：/opt/face1v1/config.toml，最后执行systemctl start supervisord启动服务。
1:N 服务监听于39389
安装完成！

```


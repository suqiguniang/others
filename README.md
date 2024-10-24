index.html:这是ariaNg单文件版本.  
https://suqiguniang.github.io/.  
柒柒的图片存储.  

# 存放大多数的小文件


```
img2kvm
pve下img写入disk脚本
使用示例
./imgkvm xxx.img vm-disk-1 local-lvm 100
位置:/others/img2kvm
```

```
move.sh
aria2-Pro的移动文件脚本，用于aria2-pro下载完成后自动根据后缀名分类文件
位置：/others/move.sh
```

```
pve_souse.tar.gz
pve_souse脚本
```

```
tool.sh
pve的又一种脚本
```

```
unrar.sh
配合crontab自动解压文件并删除文件
```

```
pve核显直通文件
n100 pve igd gop rom文件
```
```
docker run -d \
    --name aria2-pro \
    --restart unless-stopped \
    --log-opt max-size=1m \
    -e PUID=$UID \
    -e PGID=$GID \
    -e RPC_PORT=6800 \
    -p 6800:6800 \
    -e LISTEN_PORT=6888 \
    -p 6888:6888 \
    -p 6888:6888/udp \
    p3terx/aria2-pro
```


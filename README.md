index.html:这是ariaNg单文件版本.  
https://suqiguniang.github.io/.  
柒柒的图片存储.  

# 存放大多数的小文件

## pve脚本
```
img2kvm
pve下img写入disk脚本
使用示例
./imgkvm xxx.img vm-disk-1 local-lvm 100
位置:/others/img2kvm
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
pve核显直通文件
n100 pve igd gop rom文件
```
## aria2-pro脚本
```
move.sh
aria2-Pro的移动文件脚本，用于aria2-pro下载完成后自动根据后缀名分类文件
位置：/others/move.sh

aria2.conf
aria2-Pro的配置文件
```

## 个人脚本
```
unrar.sh
配合crontab自动解压文件并删除文件
cosplaytele
```
## docker备份
### aria2-pro
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
### clash
```
docker run -d \
  --name clash \
  --restart=always \
  --log-opt max-size=1m \
  -v /root/clash/clash.yaml:/root/.config/clash/config.yaml \
  -p 9090:8080 -p 7890:7890 \
  laoyutang/clash-and-dashboard:latest
```
### speedtest
```
docker run -d \
  --name speedtest \
  --restart=always \
  -p 40080:80  \
  ghcr.io/librespeed/speedtest:latest
```
### natfrp
```
docker run \
   -d \
   --network=host \
   --restart=on-failure:5 \
   --pull=always \
   --name=natfrp-service \
   -e "NATFRP_TOKEN=<访问密钥>" \
   -e "NATFRP_REMOTE=<设定一个远程管理密码，最少8个字符>" \
   natfrp.com/launcher
```
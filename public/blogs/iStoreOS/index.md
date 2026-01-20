# iStoreOS
## 1.修改端口号
```
cd /etc/config/
```
```
vim uhttpd
```
### ps:按:wq!reboot重启生效
## 2.安装docker compose
```
opkg update
```
```
opkg install docker-compose
```
## 3.解决opkg不能安装的问题
```
vim /etc/opkg.conf  #注释或删掉 /etc/opkg.conf 中的 option check_signature
```
```
 vim /etc/opkg/compatfeeds.conf #后面加src/gz openwrt_dllkids https://op.dllkids.xyz/packages/x86_64/
```
```
opkg update
```
```
opkg install luci-app-xxx
```
### 软件库
```
https://op.dllkids.xyz/packages/x86_64/
https://dl.openwrt.ai/packages-23.05/x86_64/
```





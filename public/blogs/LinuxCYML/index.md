# ❶一键安装依赖
## 1.Debian/Ubuntu系统
```
apt update -y&&apt install -y curl&&apt install -y socat
```
## 2.CentOS系统
```
yum update -y&&yum install -y curl&&yum install -y socat 
```
# ❷UFW防火墙
### 1.一键放行22端口
```
apt install ufw && ufw allow 22/tcp && ufw enable
```
### 2.删除放行80端口
```
sudo ufw delete allow 80/tcp
```
### 3.查看和删除编号端口
#### 查看放行端口[不带编号]
```
sudo ufw status verbose
```
#### 查看放行端口[带编号]
```
sudo ufw status numbered
```
#### 删除编号1的端口
```
sudo ufw delete 1
```
# ❸创建和删除文件
```
mkdir /mnt/data_vdb1
```
```
rm /mnt/data_vdb1
```
# ❹查找文件和文件夹
```
sudo find / -type d -name "aria2"
```
```
sudo find / -type f -iname "aria2.conf" 2>/dev/null
```



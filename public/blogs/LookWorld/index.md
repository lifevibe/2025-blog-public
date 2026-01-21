# ❶3-XUI
## 1.面板安装
```
bash <(curl -Ls https://raw.githubusercontent.com/xeefei/3x-ui/master/install.sh)
```
* 如果要申请安装证书并每3个月【自动续签】证书，请确保80和443端口是放行打开的
## 2.面板设置

> 1、已经安装证书的【路径】，位置在：/root/.acme.sh/（域名）_ecc；
2、进入后台【面板设置】—–>【常规】中，去分别填入刚才已经记录的证书公钥、私钥路径；
3、点击左上角的【保存】和【重启面板】，即可用自己域名进行登录管理。
4、再次登录面板：域名:端口/路径
* PS：若你在正确完成了上述步骤之后，你没有安装证书的情况下，去用IP+端口号/路径的方式却不能访问面板，那请检查一下是不是你的浏览器自动默认开启了https模式，需要手动调整一下改成http方式，把“s”去掉，即可访问成功。
## 3.入站规则
> 点击左边【入站列表】，然后【添加入站】，传输方式保持【TCP】不变,尽量选择主流的vless+reality+vision协议组合，在创建reality协议过程中,至于其他诸如：PROXY Protocol，HTTP 伪装，TPROXY，External Proxy等等选项，若无特殊要求，保持默认设置即可，不用去动它们,其他：流量限制，到期时间，客户TG的ID等选项根据自己需求填写
* PS：一定要放行端口之后，确保端口能够ping通，再导入软件节点配置及功能方面
# ❷Hysteria2
## 1.系统组件升级至最新：
```
apt update -y && apt install -y curl && apt install -y socat
```
## 2.Hysteria 2 一键安装脚本
```
wget -N --no-check-certificate https://raw.githubusercontent.com/flame1ce/hysteria2-install/main/hysteria2-install-main/hy2/hysteria.sh && bash hysteria.sh
```
## 3.查看 hysteria 服务 状态
```
systemctl status hysteria-server.service
```
##  4.启动 hysteria 服务
```
systemctl start hysteria-server.service
```
##  5.设置 hysteria 服务 开机自启
```
systemctl enable hysteria-server.service
```
## 6.其他常用命令
### 1.停止 hysteria 服务
```
systemctl stop hysteria-server.service
```
### 2.重启 hysteria 服务
```
systemctl restart hysteria-server.service
```

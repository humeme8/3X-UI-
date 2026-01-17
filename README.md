# 零基础小白3X-UI搭建教程，轻松搭建专属VPS节点

<img width="900" height="611" alt="4d3ae628-9aac-4b8b-94cb-b91e6b2241c6" src="https://github.com/user-attachments/assets/f7a63f25-dad5-4175-bb97-7ad319f86dd6" />

3x-ui是一个支持多协议、多用户的Xray内核面板，具有过期日期、流量和IP限制功能。它能够同时支持Vmess、Vless、Trojan、ShadowSocks和Wireguard等多种协议，为用户提供更灵活的选择。且对小白特别友好，通过简单的命令即可轻松安装。轻松实现上网自由。

<br>

**一、准备工作**

<br>

1.一台vps（自行购买）

服务器环境：Ubuntu22+ / Debian12+系统

自建节点的前提是需要有一台VPS服务器，演示的为66云美国CN2 GIA专线，推荐使用（[666clouds](https://www.666clouds.com/aff.php?aff=3554)），不满意支持退款。

2.SSH远程工具

FinalShell(推荐):[FinalShell](https://www.hostbuf.com/t/988.html)

3.代理软件

电脑端推荐：[v2rayN](https://github.com/2dust/v2rayN/releases/tag/7.17.0)  推荐下载【v2rayN-windows-64-SelfContained.zip版】

安卓手机推荐：[NekoBox](https://github.com/MatsuriDayo/NekoBoxForAndroid/releases/tag/1.4.1)

IOS推荐：[shadowrocket（小火箭）](https://apps.apple.com/app/shadowrocket/id932747118)

<br>

**二、搭建过程**
<br>
<br>
3X-UI开源地址：[https://github.com/MHSanaei/3x-ui](https://github.com/MHSanaei/3x-ui)

搭建前，先检测服务器IP是否被墙，确认IP可用。
电脑Win+R 输入 CMD 回车：键入ping 空格 输入你的ip，检查一下是否可以 ping 通。

或登录网站[ping.pe ](https://ping.pe/)测试，下拉查看国内节点是否全是绿色，站长工具 [itdog.cn](https://www.itdog.cn/ping/)输入ip，单次测试是否全绿色。

通过FinalShell 连接上VPS后，分别执行以下命令

<br>

1.服务器系统更新及安装组件：

<br>

```bash
apt update -y && apt install -y curl && apt install -y socat
```
<br>

一键安装部署3X-UI代码命令：

<br>

```bash
bash <(curl -Ls https://raw.githubusercontent.com/mhsanaei/3x-ui/master/install.sh)
```



<br>

**安装过程**

<br>
1.安装过程中出现选择（Y/N） 询问是否自定义面板端口，默认随机端口，回车

2.出现ssl证书安装选择：

（1）为域名安装----如果你有域名这里选择1

（2）为ip地址安装----没有域名选择2

3.出现询问是否要包含IP6地址，回车跳过，如果你上一步是域名，这步是输入你的域名。

4.出现设置http端口，默认80，使用默认，回车。

5.安装完成后会显示默认的：

Username：用户名

Password：密码

Port：端口

WebBasePath：路径

Aceess URL：面板访问地址

----后面也可在面板设置更改！

<br>

**开启BBR加速**

<br>

远程管理输入命令： x-ui

输入数字23，选择两次1，开启BBR加速。

<br>

**登录3x-UI面板**

<br>

（1）登录面板：https://域名:端口/根路径

（2）添加节点：点击入站列表→添加入站

①组合1：vless+TCP+Reality

备注：任意

协议：选择vless

端口：随机

传输：选择TCP

安全：选reality

Target/SNI：默认（如是Google.com，改成yahoo.com、tesla.com、amd.com、bing.com、ntel.com等）

点击【Get New Cert】获取公钥和私钥

②组合2：vless+XHTTP+Reality

备注：任意

协议：选择vless

端口：随机

传输：选择XHTTP

路径：任意设置，英文

安全：选reality

Target/SNI：默认（如是Google.com，改成yahoo.com、tesla.com、amd.com、bing.com、ntel.com等）

点击【Get New Cert】获取公钥和私钥

<br>

**导入节点**

<br>

扫描二维码、或复制粘贴链接导入客户端

<br>
<br>
**郑重声明：请合理使用科学上网，用于学习、科研、外贸等，严格遵守当地相关规定！**

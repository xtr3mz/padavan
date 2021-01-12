本人的Release中的文件为Newifi3 d2的固件！仅有这个
原固件bug 死机重启会卡住，只能拔电源，所以我也不用了

### 修改文件如下，可自行添加 ###
* /state.js（中间菜单，和末尾mobilestyle ）
* /bootstrap/main.css (末尾 media screen)
* /nologin.html
* /login.html

### 效果图 ###

![image](https://github.com/xtr3mz/padavan/raw/master/%E6%9C%AA%E6%A0%87%E9%A2%98-1.jpg)


###以下整理自hanwckf的padavan###

![CI](https://github.com/hanwckf/rt-n56u/workflows/CI/badge.svg)
![GitHub All Releases](https://img.shields.io/github/downloads/hanwckf/rt-n56u/total)
[![release](https://img.shields.io/github/release/hanwckf/rt-n56u.svg)](https://github.com/hanwckf/rt-n56u/releases)

# 介绍 #
本项目为路由器固件，意为改善 rt-n56u 类似型号路由器的使用体验，提供了插件和功能改进。
总而言之，我们的意图是好的，但是，刷机风险自担（首先确保你刷了breed）。

### 原始项目地址 ###
* [Get the tools to build the system](https://bitbucket.org/padavan/rt-n56u/wiki/EN/HowToMakeFirmware) 
* [Download pre-built system image](https://bitbucket.org/padavan/rt-n56u/downloads)

***

### 特别说明 ###
* 汉化字典来自：https://github.com/gorden5566/padavan
* 更新日志：https://www.jianshu.com/p/d76a63a12eae
* 使用[gorden5566](https://github.com/gorden5566/padavan)的汉化字典
* aria2 前端管理更换为[AriaNg](https://github.com/mayswind/AriaNg)
* [curl](https://github.com/curl/curl)可选编译可执行程序 ```CONFIG_FIRMWARE_INCLUDE_CURL```
* 使用了[PROMETHEUS](http://pm.freize.net/index.html)提供的部分补丁
* 使用了[Linaro1985/padavan-ng](https://gitlab.com/padavan-ng/padavan-ng)的部分软件包
***

### 可选插件(可不装，不影响基本功能) ###
配置文件内修改，文件在/opt/rt-n56u/trunk/configs/templates/(你的路由型号).config
- 工具1：
>- KMS /地址已丢失 [vlmcsd] (https://github.com/hanwckf/vlmcsd) ```CONFIG_FIRMWARE_INCLUDE_VLMCSD```
>- 局域网共享文件 [samba3.6](https://gitlab.com/padavan-ng/padavan-ng/tree/master/trunk/user/samba36) ```CONFIG_FIRMWARE_INCLUDE_SMBD36```
>- IPV6端口转发 [napt66](https://github.com/mzweilin/napt66) ```CONFIG_FIRMWARE_INCLUDE_NAPT66```
>- Aria2 HTTP/BT 下载工具
>- Transmission BT 下载工具

- 工具2：
>- 限速 ```CONFIG_FIRMWARE_INCLUDE_IMQ/IFB```
>- Webshell [ttyd](https://github.com/tsl0922/ttyd) ```CONFIG_FIRMWARE_INCLUDE_TTYD```
>- 兼容x/y/zmodem/文件传输 [lrzsz](https://ohse.de/uwe/software/lrzsz.html) ```CONFIG_FIRMWARE_INCLUDE_LRZSZ```
>- 进程查看 [htop](https://hisham.hm/htop/releases/) ```CONFIG_FIRMWARE_INCLUDE_HTOP```
>- 网络诊断 [mtr](https://github.com/traviscross/mtr) ```CONFIG_FIRMWARE_INCLUDE_MTR```
>- 文本编辑器 [nano](https://www.nano-editor.org/dist/) ```CONFIG_FIRMWARE_INCLUDE_NANO```
>- 网络性能测试 [iperf3](https://github.com/esnet/iperf) ```CONFIG_FIRMWARE_INCLUDE_IPERF3```
>- 多功能网络工具 [socat](http://www.dest-unreach.org/socat) ```CONFIG_FIRMWARE_INCLUDE_SOCAT```

-  登录客户端：
>- 校园网 [scutclient](https://github.com/hanwckf/scutclient) ```CONFIG_FIRMWARE_INCLUDE_SCUTCLIENT```
>- 锐捷认证 [mentohust](https://github.com/hanwckf/mentohust-1) ```CONFIG_FIRMWARE_INCLUDE_MENTOHUST```
>- Dr.com [gdut-drcom]D(https://github.com/chenhaowen01/gdut-drcom) ```CONFIG_FIRMWARE_INCLUDE_GDUT_DRCOM```
>- Dr.com [dogcom](https://github.com/hanwckf/dogcom) ```CONFIG_FIRMWARE_INCLUDE_DOGCOM```
>- EAP [minieap](https://github.com/hanwckf/minieap) ```CONFIG_FIRMWARE_INCLUDE_MINIEAP```
>- 南京工程 /地址已丢失 [njit-client](https://github.com/hanwckf/njit8021xclient) ```CONFIG_FIRMWARE_INCLUDE_NJIT_CLIENT```

- 无线电：
>- Mode S解码器 [dump1090](https://github.com/hanwckf/dump1090) ```CONFIG_FIRMWARE_INCLUDE_DUMP1090```
>- 解码器 [rtl-sdr](https://github.com/osmocom/rtl-sdr) ```CONFIG_FIRMWARE_INCLUDE_RTL_SDR```

- 代理：
>- [dns-forwarder](https://github.com/aa65535/hev-dns-forwarder) ```CONFIG_FIRMWARE_INCLUDE_DNSFORWARDER```
>- [ssr](https://github.com/shadowsocksr-backup/shadowsocksr-libev)/[ss](https://github.com/shadowsocks/shadowsocks-libev) ```CONFIG_FIRMWARE_INCLUDE_SHADOWSOCKS```
>- [ss-server](https://github.com/shadowsocks/shadowsocks-libev) ```CONFIG_FIRMWARE_INCLUDE_SSSERVER```
>- [softether-vpnserver](https://github.com/SoftEtherVPN/SoftEtherVPN_Stable) ```CONFIG_FIRMWARE_INCLUDE_SOFTETHERVPN_SERVER```
>- [softether-vpnclient](https://github.com/SoftEtherVPN/SoftEtherVPN_Stable) ```CONFIG_FIRMWARE_INCLUDE_SOFTETHERVPN_CLIENT```
>- [softether-vpncmd](https://github.com/SoftEtherVPN/SoftEtherVPN_Stable) ```CONFIG_FIRMWARE_INCLUDE_SOFTETHERVPN_CMD```

>- socks4/5服务器 [srelay](https://socks-relay.sourceforge.io) ```CONFIG_FIRMWARE_INCLUDE_SRELAY```
>- 代理服务器 [3proxy](https://github.com/z3APA3A/3proxy) ```CONFIG_FIRMWARE_INCLUDE_3PROXY```
>- 反向代理 [frpc](https://github.com/fatedier/frp) ```CONFIG_FIRMWARE_INCLUDE_FRPC```
>- 反向代理 [frps](https://github.com/fatedier/frp) ```CONFIG_FIRMWARE_INCLUDE_FRPS```
>- W

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
>- WireGuard客户端 [tunsafe](https://github.com/TunSafe/TunSafe) ```CONFIG_FIRMWARE_INCLUDE_TUNSAFE```
>- WireGuard客户端/GO语言 [wireguard-go](https://git.zx2c4.com/wireguard-go/) ```CONFIG_FIRMWARE_INCLUDE_WIREGUARD```

- 已适以下机型
>- 360P2 (USB)
>- 5K-W20 (USB)
>- A3004NS (USB)
>- B70 (USB)
>- DIR-882 (USB) / DIR-878
>- E8820V2(USB)
>- HC5661A / HC5761A (USB) / HC5861B

>- JCG-836PRO (USB) / JCG-AC860M (USB) / JCG-Y2(USB)
>- K2P / K2P-USB (USB)
>- MI-MINI (USB) / MI-3 (USB) /MI-R3G (USB) / MI-NANO
>- MR2600 (USB)
>- MZ-R13 / MZ-R13P
>- MSG1500(USB)
>- NEWIFI-MINI (USB) / NEWIFI3 (USB)

>- OYE-001 (USB)
>- PSG1208 / PSG1218
>- RM2100
>- R2100
>- RT-AC1200GU (USB)
>- WR1200JS (USB)
>- WDR7300
>- XY-C1 (USB)

***

### 编译说明 ###

* 安装依赖包

```shell
# Debian/Ubuntu/Deepin深度（推荐）
sudo apt update
sudo apt install unzip libtool-bin curl cmake gperf gawk flex bison nano xxd \
	fakeroot kmod cpio git python-docutils gettext automake autopoint \
	texinfo build-essential help2man pkg-config zlib1g-dev libgmp3-dev \
	libmpc-dev libmpfr-dev libncurses5-dev libltdl-dev wget libc-dev-bin

# Archlinux/Manjaro
sudo pacman -Syu --needed git base-devel cmake gperf ncurses libmpc \
        gmp python-docutils vim rpcsvc-proto fakeroot cpio help2man

# Alpine
sudo apk add make gcc g++ cpio curl wget nano xxd kmod \
	pkgconfig rpcgen fakeroot ncurses bash patch \
	bsd-compat-headers python2 python3 zlib-dev \
	automake gettext gettext-dev autoconf bison \
	flex coreutils cmake git libtool gawk sudo

# CentOS 7
sudo yum update
sudo yum groupinstall "Development Tools"
sudo yum install ncurses-* flex byacc bison zlib-* texinfo gmp-* mpfr-* gettext \
	libtool* libmpc-* gettext-* python-docutils nano help2man fakeroot

# CentOS 8
sudo yum update
sudo yum groupinstall "Development Tools"
sudo yum install ncurses-* flex byacc bison zlib-* gmp-* mpfr-* gettext \
	libtool* libmpc-* gettext-* nano fakeroot

# CentOS 8不能直接通过yum安装texinfo，help2man，python-docutils。请去官网下载发行的安装包编译安装
# 以texinfo为例
# cd /usr/local/src
# sudo wget http://ftp.gnu.org/gnu/texinfo/texinfo-6.7.tar.gz
# sudo tar zxvf texinfo-6.7.tar.gz
# cd texinfo-6.7
# sudo ./configure
# sudo make
# sudo make install

```

* 克隆源码

```shell
git clone --depth=1 https://e.coding.net/hanwckf/rt-n56u/padavan.git /opt/rt-n56u
#github 太慢
#git clone --depth=1 https://github.com/hanwckf/rt-n56u.git /opt/rt-n56u
```

* 准备工具链

```shell
cd /opt/rt-n56u/toolchain-mipsel

# （推荐）下载工具链：
# 注意：github下载慢的，打开dl_toolchain.sh源码
# 从源码中地址下载 mipsel-linux-uclibc.tar.xz到本地，然后执行源码中的mkdir和tar

sh dl_toolchain.sh

# 如果文件下不了，就自己编译，需要一些时间：（虚拟机4核编译时间98分）
./clean_toolchain
./build_toolchain

```

* 以下代码中的 PSG1218 为路由型号
* 请将 PSG1218 修改为自己的路由型号，具体型号在trunk/configs/templates/中找
* (可选) 用nano编辑器修改配置文件（例如：编译 PSG1218路由固件）
```shell
nano /opt/rt-n56u/trunk/configs/templates/PSG1218.config
```
* 清理文件（首次编译无需清理，换路由器型号，需要清理）
```shell
cd /opt/rt-n56u/trunk
./clear_tree
```

* 开始编译（例如：编译 PSG1218路由固件）
```shell
# 对于WSL环境，建议使用sudo进行编译，或者使用fakeroot-tcp代替fakeroot
fakeroot ./build_firmware_modify PSG1218

```
* 编译好的固件在trunk/images里

***

### 编译步骤请参阅 ###
- https://www.jianshu.com/p/cb51fb0fb2ac
- https://www.jianshu.com/p/6b8403cdea46

### 图形界面管理 & 编辑文件（root模式）
* 新装系统需要设root密码，输入命令，然后输入2次密码即可
```shell 
sudo passwd
```

* root模式文件浏览器，在命令窗口输入：
* debian/ubuntu： sudo nautilus
* deepin/深度系统：sudo dde-file-manager

* 打开系统盘（ubuntu: 其他位置->我的电脑），在opt里可看到rt-n56u文件夹

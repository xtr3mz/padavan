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

### 可选插件 ###
-  登录客户端：
>- [scutclient]校园网(https://github.com/hanwckf/scutclient) ```CONFIG_FIRMWARE_INCLUDE_SCUTCLIENT```
>- [mentohust]锐捷认证(https://github.com/hanwckf/mentohust-1) ```CONFIG_FIRMWARE_INCLUDE_MENTOHUST```
>- [gdut-drcom]Dr.com(https://github.com/chenhaowen01/gdut-drcom) ```CONFIG_FIRMWARE_INCLUDE_GDUT_DRCOM```
>- [dogcom]Dr.com(https://github.com/hanwckf/dogcom) ```CONFIG_FIRMWARE_INCLUDE_DOGCOM```
>- [minieap]EAP(https://github.com/hanwckf/minieap) ```CONFIG_FIRMWARE_INCLUDE_MINIEAP```
>- [njit-client]南京工程 /地址已丢失 (https://github.com/hanwckf/njit8021xclient) ```CONFIG_FIRMWARE_INCLUDE_NJIT_CLIENT```

- 工具：
>- [ttyd]Webshell(https://github.com/tsl0922/ttyd) ```CONFIG_FIRMWARE_INCLUDE_TTYD```
>- [lrzsz]兼容x/y/zmodem/文件传输(https://ohse.de/uwe/software/lrzsz.html) ```CONFIG_FIRMWARE_INCLUDE_LRZSZ```
>- [htop]进程查看(https://hisham.hm/htop/releases/) ```CONFIG_FIRMWARE_INCLUDE_HTOP```
>- [mtr]网络诊断(https://github.com/traviscross/mtr) ```CONFIG_FIRMWARE_INCLUDE_MTR```
>- [nano]文本编辑器(https://www.nano-editor.org/dist/) ```CONFIG_FIRMWARE_INCLUDE_NANO```
>- [iperf3]网络性能测试(https://github.com/esnet/iperf) ```CONFIG_FIRMWARE_INCLUDE_IPERF3```
>- [socat]多功能网络工具(http://www.dest-unreach.org/socat) ```CONFIG_FIRMWARE_INCLUDE_SOCAT```
- 无线电：
>- [dump1090]Mode S解码器(https://github.com/hanwckf/dump1090) ```CONFIG_FIRMWARE_INCLUDE_DUMP1090```
>- [rtl-sdr]解码(https://github.com/osmocom/rtl-sdr) ```CONFIG_FIRMWARE_INCLUDE_RTL_SDR```
- 工具：
>- [vlmcsd]KMS /地址已丢失 (https://github.com/hanwckf/vlmcsd) ```CONFIG_FIRMWARE_INCLUDE_VLMCSD```
>- [samba3.6]局域网共享文件(https://gitlab.com/padavan-ng/padavan-ng/tree/master/trunk/user/samba36) ```CONFIG_FIRMWARE_INCLUDE_SMBD36```

- 代理：
>- [dns-forwarder](https://github.com/aa65535/hev-dns-forwarder) ```CONFIG_FIRMWARE_INCLUDE_DNSFORWARDER```
>- [napt66]IPV6端口转发(https://github.com/mzweilin/napt66) ```CONFIG_FIRMWARE_INCLUDE_NAPT66```
>- [ssr](https://github.com/shadowsocksr-backup/shadowsocksr-libev)/[ss](https://github.com/shadowsocks/shadowsocks-libev) ```CONFIG_FIRMWARE_INCLUDE_SHADOWSOCKS```
>- [ss-server](https://github.com/shadowsocks/shadowsocks-libev) ```CONFIG_FIRMWARE_INCLUDE_SSSERVER```
>- [softether-vpnserver](https://github.com/SoftEtherVPN/SoftEtherVPN_Stable) ```CONFIG_FIRMWARE_INCLUDE_SOFTETHERVPN_SERVER```
>- [softether-vpnclient](https://github.com/SoftEtherVPN/SoftEtherVPN_Stable) ```CONFIG_FIRMWARE_INCLUDE_SOFTETHERVPN_CLIENT```
>- [softether-vpncmd](https://github.com/SoftEtherVPN/SoftEtherVPN_Stable) ```CONFIG_FIRMWARE_INCLUDE_SOFTETHERVPN_CMD```

>- [srelay]socks4/5服务器(https://socks-relay.sourceforge.io) ```CONFIG_FIRMWARE_INCLUDE_SRELAY```
>- [3proxy]代理服务器(https://github.com/z3APA3A/3proxy) ```CONFIG_FIRMWARE_INCLUDE_3PROXY```
>- [frpc]反向代理(https://github.com/fatedier/frp) ```CONFIG_FIRMWARE_INCLUDE_FRPC```
>- [frps]反向代理(https://github.com/fatedier/frp) ```CONFIG_FIRMWARE_INCLUDE_FRPS```
>- [tunsafe]WireGuard客户端(https://github.com/TunSafe/TunSafe) ```CONFIG_FIRMWARE_INCLUDE_TUNSAFE```
>- [wireguard-go]WireGuard/GO语言(https://git.zx2c4.com/wireguard-go/) ```CONFIG_FIRMWARE_INCLUDE_WIREGUARD```

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

# 如果文件下不了，就自己编译，需要一些时间：
./clean_toolchain
./build_toolchain

```

* 以下代码中的 PSG1218 为路由型号
* 请将 PSG1218 修改为自己的路由型号，具体型号在trunk/configs/templates/中找
* (可选) 用nano编辑器修改配置文件（例如：编译 PSG1218路由固件）
```shell
nano /opt/rt-n56u/trunk/configs/templates/PSG1218.config
```

* 清理并开始编译（例如：编译 PSG1218路由固件）

```shell
cd /opt/rt-n56u/trunk
./clear_tree
# 对于WSL环境，建议使用sudo进行编译，或者使用fakeroot-tcp代替fakeroot
fakeroot ./build_firmware_modify PSG1218

```
* 编译好的固件在trunk/images里

***

### 编译步骤请参阅 ###
- https://www.jianshu.com/p/cb51fb0fb2ac
- https://www.jianshu.com/p/6b8403cdea46


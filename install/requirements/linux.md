---
title: Linux Requirements
description: 
published: true
date: 2025-07-01T14:03:14.958Z
tags: requirements, installation, setup, linux
editor: markdown
dateCreated: 2021-08-14T00:09:23.038Z
---

## Software
>Processor with SSE2 support 
>Boost ≥ 1.74
>MySQL ≥ 5.7 ≤ 8.3
>OpenSSL ≥ 3.x
>CMake ≥ 3.24
>Clang  ≥ 11 (heavy recommended, especially on master branch) or GCC ≥ 11.1
>zlib ≥ 1.2.7
{.is-info}


>**Note:**
>While compiling you may get an error like: 
`c++: internal compiler error: Killed (program cc1plus)` 
>
>Reasons for this might be:
>- Low ram/swap amount: increase ram/swap to a minimum of 2GB of ram and 2GB of swap or decrease the amount of make -j to 1 (more concurrent compile threads = more memory usage). (you can get this using VPS servers)
>- SELinux/grsecurity/Hardened kernel: Kernels that use ASLR as a security measure tend to mess up GCC's precompiled header implementation. Try using an unhardened kernel (without ASLR), or compiling using clang, or gcc without pch. (you can get this issue when using OVH hosting).
>
>
>
>Your server may be abruptly killed by an angry administrator, system staff, or system restrictions for overuse of system resources. You may see something like:
>
>`collect2: fatal error: ld terminated with signal 9 [Killed] compilation terminated.`
>
>You will need to use less jobs (make -j1) or increase swap.
{.is-warning}

## OS
## Linux {.tabset}
### Debian based distributions
***(heavy recommended debian stable, it's the distribution we use to set minimum requirements)***

**Recommendation:** Use apt-get with stable source list instead of install packages. We recommend the latest stable version of your distribution. We usually update requirements to the lastest stable Debian version. Avoid mixing stable with experimental packages as it may break your linux OS.

Debian 12.x (you will need to use su to install the packages)
<div class="next-codeblock-no-line-numbers"></div>

```bash
# For latest mysql-apt repository, check url from https://dev.mysql.com/downloads/repo/apt/
wget https://dev.mysql.com/get/mysql-apt-config_0.8.29-1_all.deb -O /tmp/mysql-apt-config_all.deb
DEBIAN_FRONTEND=noninteractive dpkg -i /tmp/mysql-apt-config_all.deb
apt-get update
apt-get install git clang cmake make gcc g++ libmysqlclient-dev libssl-dev libbz2-dev libreadline-dev libncurses-dev libboost-all-dev mysql-server p7zip
update-alternatives --install /usr/bin/cc cc /usr/bin/clang 100
update-alternatives --install /usr/bin/c++ c++ /usr/bin/clang 100
```

Ubuntu 22.04 (you will need to use sudo to install the packages)
<div class="next-codeblock-no-line-numbers"></div>

```bash
apt-get update
apt-get install git clang cmake make gcc g++ libmysqlclient-dev libssl-dev libbz2-dev libreadline-dev libncurses-dev libboost-all-dev mysql-server p7zip
update-alternatives --install /usr/bin/cc cc /usr/bin/clang 100
update-alternatives --install /usr/bin/c++ c++ /usr/bin/clang 100
```

> Anything under this is not tested by TrinityCore developers.
> 
> **Not supported:** Debian 11 or lower. Ubuntu 20.04 or lower.
> 
> AVOID CentOS.
> 
> If you have an old Ubuntu version, follow https://help.ubuntu.com/community/Upgrades steps to upgrade it.
{.is-info}

### Fedora based distributions
Tested on Fedora 40
<div class="next-codeblock-no-line-numbers"></div>

```bash
dnf install https://dev.mysql.com/get/mysql84-community-release-fc40-1.noarch.rpm
dnf install git clang cmake make gcc gcc-c++ community-mysql-devel openssl-devel bzip2-devel readline-devel ncurses-devel boost-devel community-mysql-server p7zip
rm -f /usr/bin/c++
update-alternatives --install /usr/bin/cc cc /usr/bin/clang 100
update-alternatives --install /usr/bin/c++ c++ /usr/bin/clang 100
```

### Red Hat based distributions outdated

> NOT SUPPORTED!
{.is-danger}

<div class="next-codeblock-no-line-numbers"></div>

```bash
yum install epel-release
yum install git cmake3 make clang mariadb-devel openssl-devel bzip2-devel readline-devel ncurses-devel gcc-c++
ln -s /usr/bin/cmake3 /usr/bin/cmake
yum install centos-release-scl
yum install devtoolset-6-gcc-c++
scl enable devtoolset-6 bash
gcc --version | head -1
 
yum install libquadmath-devel python-devel
curl -L https://dl.bintray.com/boostorg/release/1.64.0/source/boost_1_64_0.tar.gz -o boost_1_64_0.tar.gz
tar -zxvf boost_1_64_0.tar.gz
cd boost_1_64_0
./bootstrap.sh
./b2 install
 
yum install mariadb-server p7zip 
```
> **Note:** You will only have to compile the boost library one time, unless you update your kernel or update certain security packages. You will also need to update boost-devel. The developer libraries will conflict with the compiled version of boost on Red Hat distros. Also be sure to install boost-devel after compiling latest version of boost.
{.is-info}


> **Note:** Some distribution versions might not match our requirements for CMake. If you can't install the EPEL repository on your build server, use the following instructions to install CMake manually.
>
><div class="next-codeblock-no-line-numbers"></div>
>
>```bash
>curl https://cmake.org/files/v3.6/cmake-3.6.1.tar.gz -o cmake-3.6.1.tar.gz
>tar -zxvf cmake-3.6.1.tar.gz
>cd cmake-3.6.1
>./bootstrap
>make
>make install
>```
{.is-info}


### Arch Linux based distributions outdated

> NOT SUPPORTED!
> FOLLOW AT YOUR OWN RISK!
{.is-danger}

Tested on 2/19/2020. If you run into any issues with the dependencies don't report it to the TrinityCore team, report it to me on through email at paulrblack.prb@gmail.com
<div class="next-codeblock-no-line-numbers"></div>

```bash
pacman -S git clang cmake make gcc openssl bzip2 readline ncurses boost p7zip rpcsvc-proto
mkdir ~/mysql-tmp
cd ~/mysql-tmp
wget https://aur.archlinux.org/cgit/aur.git/snapshot/mysql57.tar.gz # Note if this no longer exists go here and download the snapshot https://aur.archlinux.org/packages/mysql57/
tar -xf mysql57.tar.gz
cd mysql57
makepkg
sudo pacman -U libmysqlclient57-5.7.29-1-x86_64.pkg.tar.xz mysql-clients57-5.7.29-1-x86_64.pkg.tar.xz mysql57-5.7.29-1-x86_64.pkg.tar.xz
cd ~
rm -rf ./mysql-tmp
```
Or if you have yay installed, you can follow this instead
<div class="next-codeblock-no-line-numbers"></div>

```bash
pacman -S --needed git clang cmake make gcc openssl bzip2 readline ncurses boost p7zip rpcsvc-proto
yay -S mysql57
```
Then initialize your MySQL database
<div class="next-codeblock-no-line-numbers"></div>

```bash
sudo mysql_install_db --user=mysql --basedir=/usr --datadir=/var/lib/mysql
```

## Help
If you still have any problem, check:

Updating or starting with TrinityCore issues, Trouble with your TrinityCore Install / Readme 1st / FAQs
Ask help on the Forum
If you still have problems, you can try to ask help on IRC, but remember it's not real time 24/7 support, most of people there lives on GMT and they can be sleeping or working.

<a href="https://trinitycore.info/en/install/Core-Installation/linux-core-installation" class="mt-5 v-btn v-btn--depressed v-btn--flat v-btn--outlined theme--light v-size--default darkblue--text text--lighten-3"><span class="v-btn__content"><span>Continue to 'Core Installation'</span><i aria-hidden="true" class="v-icon notranslate v-icon--right mdi mdi-arrow-right theme--light"></i></span></a>

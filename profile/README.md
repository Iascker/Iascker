Tutorial Creating a build environment
-------------------------------------

### Sync ###

----------------------------------
Update the linux
```bash 
sudo apt update -y && sudo apt upgrade -y
```
Install git
```bash
sudo apt install git-core -y
```
Sync your git account
```bash
git config --global user.email "mezackisilva@gmail.com"
git config --global user.name "M3zaque"
```
(optional) install and configure zsh
```bash
sudo apt install zsh -y
wget https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh
sh install.sh
```
```bash
sudo nano .zshrc
```
```bash
sudo nano /etc/passwd
```
Install python and system dependencies
```bash
sudo apt-get install 2to3 -y && sudo apt-get install python2-minimal:i386 -y && sudo apt-get install python2:i386 -y && sudo apt-get install python2-minimal -y && sudo apt-get install python2 -y && sudo apt-get install dh-python -y && sudo apt-get install python-is-python3 -y && sudo apt-get install python2 -y && sudo apt-get install python3 -y && sudo apt-get install python3.9 -y && sudo apt-get install python3.10 -y && sudo apt-get install python3.11 -y && sudo apt-get install python3-pip -y && git clone https://github.com/akhilnarang/scripts --depth 1 && cd scripts && bash setup/android_build_env.sh
```
Configure the repo command
```bash
mkdir ~/.bin
PATH=~/.bin:$PATH
curl http://commondatastorage.googleapis.com/git-repo-downloads/repo > ~/.bin/repo
chmod a+x ~/.bin/repo
export USE_CCACHE=1
export CCACHE_DIR=/home/aos/.ccache
ccache -M 100G
```
Install zram config
```bash
sudo apt-get install zram-config
```
Sync an ssh key to git
```bash
ssh-keygen -t ed25519 -C "mezackisilva@gmail.com"
```
```bash
cat /home/aos/.ssh/id_ed25519.pub
```
```bash
mkdir vos
cd vos
repo init -u https://github.com/VoltageOS/manifest.git -b 13
repo sync -c -j16 --force-sync --no-clone-bundle --no-tags
git clone git@github.com:M3zaque/device_xiaomi_lisa.git device/xiaomi/lisa
git clone git@github.com:M3zaque/kernel_xiaomi_lisa.git kernel/xiaomi/lisa
git clone git@github.com:M3zaque/vendor_xiaomi_lisa.git vendor/xiaomi/lisa
git clone git@github.com:M3zaque/device_xiaomi_lisa-miuicamera.git -b thirteen device/xiaomi/lisa-miuicamera
git clone git@github.com:M3zaque/vendor_xiaomi_lisa-miuicamera.git -b thirteen vendor/xiaomi/lisa-miuicamera
. build/envsetup.sh && brunch lisa
```
### Sync ###

----------------------------------

[![TG chat](https://img.shields.io/badge/Support-Telegram-%23e52c5f.svg?style=for-the-badge&logo=telegram&&labelColor=121217991103595)](https://t.me/M3zaque)

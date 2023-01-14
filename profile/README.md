Tutorial Creating a build environment
-------------------------------------

### Sync ###

----------------------------------

```bash
sudo apt update -y
sudo apt upgrade -y
sudo apt install git-core -y
git config --global user.email "mezackisilva@gmail.com"
git config --global user.name "M3zaque"
sudo apt-get install 2to3 -y
sudo apt-get install python2-minimal:i386 -y
sudo apt-get install python2:i386 -y
sudo apt-get install python2-minimal -y
sudo apt-get install python2 -y
sudo apt-get install dh-python -y
sudo apt-get install python-is-python3 -y
sudo apt-get install python2 -y
sudo apt-get install python3 -y
sudo apt-get install python3.9 -y
sudo apt-get install python3.10 -y
sudo apt-get install python3.11 -y
sudo apt-get install python3-pip -y
git clone https://github.com/akhilnarang/scripts --depth 1
cd scripts
bash setup/android_build_env.sh
mkdir ~/.bin
PATH=~/.bin:$PATH
curl http://commondatastorage.googleapis.com/git-repo-downloads/repo > ~/.bin/repo
chmod a+x ~/.bin/repo
export USE_CCACHE=1
export CCACHE_DIR=/home/aos/.ccache
ccache -M 100G
mkdir vos
cd vos
repo init -u https://github.com/VoltageOS/manifest.git -b 13
repo sync -c -j16 --force-sync --no-clone-bundle --no-tags
```
```bash
ssh-keygen -t ed25519 -C "mezackisilva@gmail.com"
```
```bash
cat /home/aos/.ssh/id_ed25519.pub
```
```bash
git clone git@github.com:M3zaque/device_xiaomi_lisa.git device/xiaomi/lisa
git clone git@github.com:Krypton-K/platform_kernel_xiaomi_lisa.git kernel/xiaomi/lisa
git clone git@github.com:M3zaque/vendor_xiaomi_lisa.git vendor/xiaomi/lisa
git clone https://gitlab.com/ALKALiKong/vendor_xiaomi_lisa-miuicamera.git -b thirteen vendor/xiaomi/lisa-miuicamera
```
```bash
. build/envsetup.sh
brunch lisa
```
```bash
sudo apt install zsh -y
wget https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh
sh install.sh
```
```bash
sudo nano /etc/passwd
```
```bash
sudo nano .zshrc
```
```bash
sudo apt-get install zram-config
```

[![TG chat](https://img.shields.io/badge/Support-Telegram-%23e52c5f.svg?style=for-the-badge&logo=telegram&&labelColor=121217991103595)](https://t.me/M3zaque)

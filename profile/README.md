Tutorial Creating a build environment
-------------------------------------

### Sync ###

----------------------------------
Update the linux
```bash 
sudo apt update -y && sudo apt upgrade -y
```
```bash 
sudo apt install git-core ccache curl zsh 2to3 python2-minimal:i386 python2:i386 python2-minimal python2 dh-python python-is-python3 python2 python3 python3.10 python3.11 python3-pip gobject-introspection gtk-doc-tools intltool libgirepository1.0-dev libgspell-1-dev libgtk-3-dev libgtksourceview-4-dev libpeas-dev libxapp-dev zram-config -y
```
Sync your git account
```bash
git config --global user.email "mezackisilva@gmail.com"
git config --global user.name "KimiNiTodock"
```
dependencies
```bash
git clone https://github.com/akhilnarang/scripts --depth 1
cd scripts
bash setup/android_build_env.sh
git clone git@github.com:KimiNiTodock/Linux-Mint-Debloater.git
cd Linux-Mint-Debloater
chmod +x debloat-mint.sh
sudo bash debloat-mint.sh
```
(optional) configure zsh
```bash
wget https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh
sh install.sh
```
```bash
sudo nano .zshrc
```
```bash
sudo nano /etc/passwd
```
Configure the repo command
```bash
mkdir ~/.bin
PATH=~/.bin:$PATH
curl http://commondatastorage.googleapis.com/git-repo-downloads/repo > ~/.bin/repo
chmod a+x ~/.bin/repo
export USE_CCACHE=1
export CCACHE_DIR=/home/aos/.ccache
ccache -M 70G
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
repo init -u https://github.com/VoltageOS/manifest.git -b 13 && repo sync -c -j16 --force-sync --no-clone-bundle --no-tags
git clone git@github.com:KimiNiTodock/android_device_xiaomi_lisa device/xiaomi/lisa
git clone git@github.com:KimiNiTodock/android_kernel_xiaomi_lisa kernel/xiaomi/lisa
git clone git@github.com:KimiNiTodock/android_vendor_xiaomi_lisa vendor/xiaomi/lisa
git clone git@github.com:KimiNiTodock/android_device_xiaomi_camera vendor/xiaomi/camera
. build/envsetup.sh && brunch lisa
```
### Sync ###

----------------------------------

[![TG chat](https://img.shields.io/badge/Support-Telegram-%23e52c5f.svg?style=for-the-badge&logo=telegram&&labelColor=121217991103595)](https://t.me/KimiNiTodock)

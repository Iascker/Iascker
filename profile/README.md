Tutorial Creating a build environment
-------------------------------------

### Sync ###

----------------------------------
```bash
sudo apt update -y && sudo apt upgrade -y && sudo apt install git-core -y
```
```bash
git clone git@github.com:Iascker/scripts.git --depth 1
cd scripts
bash setup/android_build_env.sh
```
```bash
sudo nano /etc/passwd
```
```bash
export USE_CCACHE=1
export CCACHE_DIR=/home/aos/.ccache
ccache -M 100G
```
```bash
ssh-keygen -t ed25519 -C "mezackisilva@gmail.com"
```
```bash
cat /home/aos/.ssh/id_ed25519.pub
```
```bash
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
```
```bash
mkdir vos
cd vos
repo init -u https://github.com/VoltageOS/manifest.git -b 13 && repo sync -c -j16 --force-sync --no-clone-bundle --no-tags
git clone git@github.com:Milsapz/android_device_xiaomi_lisa device/xiaomi/lisa
git clone git@github.com:ghostrider-reborn/android_kernel_xiaomi_lahaina -b topaz kernel/xiaomi/lisa
git clone https://gitlab.com/PixelOS-Devices/vendor_xiaomi_lisa.git -b thirteen vendor/xiaomi/lisa
git clone https://gitlab.com/ghostrider-reborn/proprietary_vendor_xiaomi_camera.git vendor/xiaomi/camera
. build/envsetup.sh && brunch lisa
```
### Sync ###

----------------------------------

[![TG chat](https://img.shields.io/badge/Support-Telegram-%23e52c5f.svg?style=for-the-badge&logo=telegram&&labelColor=121217991103595)](https://t.me/KimiNiTodock)

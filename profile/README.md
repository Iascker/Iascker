Tutorial Creating a build environment
-------------------------------------

### Sync ###

----------------------------------
```bash
sudo apt update -y && sudo apt upgrade -y
```
```bash
git clone git@github.com:Zyyjz/scripts.git --depth 1
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
mkdir vos
cd vos
repo init -u https://github.com/VoltageOS/manifest.git -b 13 && repo sync -c -j16 --force-sync --no-clone-bundle --no-tags
git clone git@github.com:Zyyjz/android_device_xiaomi_lisa device/xiaomi/lisa
git clone git@github.com:Zyyjz/android_kernel_xiaomi_lisa kernel/xiaomi/lisa
git clone git@github.com:Zyyjz/android_vendor_xiaomi_lisa vendor/xiaomi/lisa
git clone git@github.com:Zyyjz/android_device_xiaomi_camera vendor/xiaomi/camera
. build/envsetup.sh && brunch lisa
```
### Sync ###

----------------------------------

[![TG chat](https://img.shields.io/badge/Support-Telegram-%23e52c5f.svg?style=for-the-badge&logo=telegram&&labelColor=121217991103595)](https://t.me/KimiNiTodock)

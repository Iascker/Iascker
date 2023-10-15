Tutorial Creating a build environment
-------------------------------------

### Sync ###

----------------------------------
```bash
sudo apt update -y && sudo apt upgrade -y && sudo apt install git-core -y
```
```bash
git clone --depth 1 git@github.com:Iascker/Iascker.git -b master scripts
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
ssh-keygen -t ed25519 -C "mezaquegit@gmail.com"
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
sudo apt install python3-pylint-common -y
```
```bash
git clone git@github.com:Iascker/android_device_xiaomi_lisa device/xiaomi/lisa
git clone git@github.com:VoltageOS-Devices/android_kernel_xiaomi_lisa kernel/xiaomi/lisa
git clone git@github.com:VoltageOS-Devices/android_vendor_xiaomi_lisa vendor/xiaomi/lisa
git clone git@github.com:dasshubham762/vendor_xiaomi_camera-lisa vendor/xiaomi/camera
. build/envsetup.sh && brunch lisa
```
```
git clone git@github.com:Exynos-982X/android_vendor_samsung_beyond1lte -b 14.0 vendor/samsung/beyond1lte
git clone git@github.com:Exynos-982X/android_hardware_samsung_slsi-linaro_config -b 14.0 hardware/samsung_slsi-linaro/config
git clone git@github.com:Exynos-982X/android_hardware_samsung_slsi-linaro_exynos -b 14.0 hardware/samsung_slsi-linaro/exynos
git clone git@github.com:Exynos-982X/android_hardware_samsung_slsi-linaro_exynos5 -b 14.0 hardware/samsung_slsi-linaro/exynos5
git clone git@github.com:Exynos-982X/android_hardware_samsung_slsi-linaro_graphics -b 14.0 hardware/samsung_slsi-linaro/graphics
git clone git@github.com:Exynos-982X/android_hardware_samsung_slsi-linaro_openmax -b 14.0 hardware/samsung_slsi-linaro/openmax
git clone git@github.com:Exynos-982X/android_hardware_samsung -b 14.0 hardware/samsung
git clone git@github.com:Exynos-982X/android_device_samsung_slsi_sepolicy -b 14.0 device/samsung_slsi/sepolicy
git clone git@github.com:Exynos-982X/android_vendor_samsung_exynos9820-common -b 14.0 vendor/samsung/exynos9820-common
git clone git@github.com:Exynos-982X/android_kernel_samsung_exynos9820 -b 14.0 kernel/samsung/exynos9820
```
### Sync ###

----------------------------------

[![TG chat](https://img.shields.io/badge/Support-Telegram-%23e52c5f.svg?style=for-the-badge&logo=telegram&&labelColor=121217991103595)](https://t.me/KimiNiTodock)

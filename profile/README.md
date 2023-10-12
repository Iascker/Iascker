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
ssh-keygen -t ed25519 -C "mezackisilver@gmail.com"
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
mkdir vos
cd vos
repo init -u https://github.com/VoltageOS/manifest.git -b 13 && repo sync -c -j16 --force-sync --no-clone-bundle --no-tags
git clone git@github.com:Milsapz/android_device_xiaomi_lisa device/xiaomi/lisa
git clone git@github.com:ghostrider-reborn/android_kernel_xiaomi_lahaina -b topaz kernel/xiaomi/lisa
git clone https://gitlab.com/PixelOS-Devices/vendor_xiaomi_lisa.git -b thirteen vendor/xiaomi/lisa
git clone https://gitlab.com/ghostrider-reborn/proprietary_vendor_xiaomi_camera.git vendor/xiaomi/camera
. build/envsetup.sh && brunch lisa
```
```bash
git clone git@github.com:Exy2100-LOS/android_device_samsung_o1s.git -b lineage-20 device/samsung/o1s
git clone git@github.com:Exy2100-LOS/android_vendor_samsung_o1s.git -b lineage-20 vendor/samsung/o1s
git clone git@github.com:LineageOS/android_device_samsung_slsi_sepolicy.git -b lineage-20 device/samsung_slsi/sepolicy
git clone git@github.com:Exy2100-LOS/android_device_samsung_universal2100-common.git -b lineage-20 device/samsung/universal2100-common
git clone git@github.com:Exy2100-LOS/android_vendor_samsung_universal2100-common.git -b lineage-20 vendor/samsung/universal2100-common
git clone git@github.com:Exy2100-LOS/proprietary_vendor_firmware.git -b lineage-20 vendor/firmware
git clone git@github.com:LineageOS/android_hardware_samsung.git -b lineage-20 hardware/samsung
git clone git@github.com:Exy2100-LOS/android_kernel_samsung_o1s.git -b lineage-20 kernel/samsung/o1s
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

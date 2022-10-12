Tutorial Creating a build environment
-------------------------------------

### Sync ###

----------------------------------

```bash
sudo apt-get update -y
sudo apt-get upgrade -y
sudo apt install git-core -y
sudo apt-get install python2 -y
sudo apt-get install python3.9 -y
sudo apt-get install python3.10 -y
sudo apt-get install python3.12 -y
sudo apt-get install python3-pip -y
git config --global user.email "mezackisilva@gmail.com"
git config --global user.name "M3zaque"
sudo apt update -y && sudo apt upgrade -y
git clone https://github.com/akhilnarang/scripts --depth 1
cd scripts
bash setup/android_build_env.sh
mkdir ~/bin && PATH=~/bin:$PATH
curl http://commondatastorage.googleapis.com/git-repo-downloads/repo > ~/bin/repo
chmod a+x ~/bin/repo


```

```bash

sudo apt install zsh -y
wget https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh
sh install.sh -y
sudo nano /etc/passwd


```

```bash

ssh-keygen -t ed25519 -C "mezackisilva@gmail.com" -y
cat /home/m3zaque/.ssh/id_ed25519.pub


```

```bash
export USE_CCACHE=1
export CCACHE_DIR=/home/aos/.ccache
ccache -M 80G

```

```bash
repo init -u https://github.com/VoltageOS/manifest -b 12l
repo sync -c -j16 --force-sync --no-clone-bundle --no-tags
repo sync -c -j16 --force-sync --no-clone-bundle --no-tags
rm-rf .repo

```

```bash
git clone git@github.com:VoltageOS-Devices/android_device_xiaomi_surya.git -b 12l device/xiaomi/surya
git clone git@github.com:EliCarmo/android_kernel_xiaomi_surya.git -b 12l kernel/xiaomi/surya
git clone git@github.com:VoltageOS-Devices/android_vendor_xiaomi_surya.git -b 12l vendor/xiaomi/surya
. build/envsetup.sh && brunch surya

```



[![TG chat](https://img.shields.io/badge/Support-Telegram-%23e52c5f.svg?style=for-the-badge&logo=telegram&&labelColor=121217)](https://t.me/Cow6oy)

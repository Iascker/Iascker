Tutorial Creating a build environment
-------------------------------------

### Sync ###

----------------------------------

```bash
sudo apt update -y && sudo apt upgrade -y

sudo apt install git-core -y
git config --global user.email "mezackisilva@gmail.com"
git config --global user.name "M3zaque"

sudo apt-get install python2 -y
sudo apt-get install python3 -y
sudo apt-get install python3.12 -y
sudo apt-get install python3-pip -y

git clone https://github.com/akhilnarang/scripts --depth 1
cd scripts
bash setup/android_build_env.sh

mkdir ~/.bin && PATH=~/.bin:$PATH
curl http://commondatastorage.googleapis.com/git-repo-downloads/repo > ~/.bin/repo
chmod a+x ~/.bin/repo

sudo apt install zsh -y
wget https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh
sh install.sh
sudo nano /etc/passwd
sudo nano .zshrc

ssh-keygen -t ed25519 -C "mezackisilva@gmail.com"
cat /home/m3zaque/.ssh/id_ed25519.pub

export USE_CCACHE=1
export CCACHE_DIR=/home/aos/.ccache
ccache -M 80G

repo init -u https://github.com/LineageOS/android.git -b lineage-19.1 && repo sync -j16

```



[![TG chat](https://img.shields.io/badge/Support-Telegram-%23e52c5f.svg?style=for-the-badge&logo=telegram&&labelColor=121217)](https://t.me/Cow6oy)

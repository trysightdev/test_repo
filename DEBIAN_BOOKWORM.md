# OS Setup 
* [Nvidia](https://wiki.debian.org/NvidiaGraphicsDrivers)
```
su root
pwd
apt instal vim sudo
exit
sudo apt install lxde-core
```
```
git clone https://github.com/morrownr/88x2bu-20210702.git
cd 88x2bu-20210702/
make -j4
sudo make install
```

```
sudo sed 'i/main /main contrib non-free /g' /etc/apt/sources.list
sudo apt update
sudo apt install linux-headers-amd64 build-essential
sudo apt install nvidia-driver firmware-misc-nonfree
```
```
wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb
sudo dpkg -i google-chrome-stable_current_amd64.deb
sudo apt-get install -f
sudo dpkg -i google-chrome-stable_current_amd64.deb
```


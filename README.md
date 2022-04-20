
### Installation instruction
##### Requirements
You will need to install "make", "gcc", "kernel headers", "kernel build essentials", and "git".

For **Ubuntu**: You can install them with the following command
```bash
sudo apt-get update
sudo apt-get install make gcc linux-headers-$(uname -r) build-essential git
```

##### Installation
For all distros:
```bash
git clone git://github.com/lwfinger/rtw89.git
cd rtw89
make
sudo make install
```

##### Installation with module signing for SecureBoot
For all distros:
```bash
git clone git://github.com/lwfinger/rtw89.git
cd rtw89
make
sudo make sign-install
```

##### How to unload/reload a Kernel module
 ```bash
sudo modprobe -rv rtw89pci         #This unloads the module
sudo modprobe -v rtw89pci          #This loads the module
```

*********************************************************************************************

When your kernel changes, then you need to do the following:
```bash
cd ~/rtw89
git pull
make clean
make
sudo make install
;or
sudo make sign-install
```

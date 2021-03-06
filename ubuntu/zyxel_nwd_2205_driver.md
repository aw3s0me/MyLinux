
# Installation

Ensure you have the necessary prerequisites:

```
sudo apt-get install linux-headers-generic build-essential dkms
```

Clone this repository:

```
git clone https://github.com/pvaret/rtl8192cu-fixes.git
```

Set it up as a DKMS module:

```
sudo dkms add ./rtl8192cu-fixes
```

Build and install it (this version number may change, it is .10 as of october 19 2015

```
sudo dkms install 8192cu/1.10
```

Refresh the module list:

```
sudo depmod -a
```

Ensure the native (and broken) kernel driver is blacklisted:

```
sudo cp ./rtl8192cu-fixes/blacklist-native-rtl8192.conf /etc/modprobe.d/
```

And reboot. You're done.

# Deinstallation
```
sudo dkms uninstall 8192cu
```
Or specify version of driver:
```
sudo dkms uninstall 8192cu/1.10
```

And if you copied the modprobe blacklist
```
sudo rm /etc/modprobe.d/rtl8192cu-fixes/blacklist-native-rtl8192.conf
```

Please run the following commands:

```
sudo apt-get install --reinstall linux-image-`uname -r`
sudo modprobe snd-hda-intel
rm -r ~/.config/pulse*
pulseaudio -k
```

Also, to replace any previous configurations:

```
sudo apt-get update
mkdir PULSE
cd PULSE
apt-get download pulseaudio
ar xvf *
tar xvf dat*
sudo rm /etc/pulse/*
sudo mv etc/pulse/* /etc/pulse/
```

reboot

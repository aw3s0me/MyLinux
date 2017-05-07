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

# IF doesnt work
Do 
```
pulseaudio -vvvv
```
U must see this:
```
I: [pulseaudio] main.c: setrlimit(RLIMIT_NICE, (31, 31)) failed: Operation not permitted
I: [pulseaudio] main.c: setrlimit(RLIMIT_RTPRIO, (9, 9)) failed: Operation not permitted
```
Then it is problem with permissions

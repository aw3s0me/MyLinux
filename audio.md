# See available audio devices
```
cat /proc/asound/cards
```
OR (general, maybe something is not detected)
```
cat /proc/asound/devices
```

# Restoring audio (when Dummy Output in pulse audio)
## 1. Reinstall alsa and pulse
```
sudo update-grub
sudo apt-get remove --purge alsa-base
sudo apt-get remove --purge pulseaudio
sudo apt-get install alsa-base
sudo apt-get install pulseaudio
sudo alsa force-reload
```

AND Need to switch Configuration in pulseaudio to Analog Stereo Output

## 2. Install Pulseaudio Equalizer
```
sudo add-apt-repository ppa:nilarimogard/webupd8
sudo apt-get update
sudo apt-get install pulseaudio-equalizer
```
## 3. Install alsa-oss
use: http://www.opensound.com/download.cgi

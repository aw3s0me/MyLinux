# See video card
## Basic info
```
lspci | grep VGA
```
## Detailed info
```
sudo lshw -C video
```
## GUI version
first install lshw-gtk
```
sudo apt-get install lshw-gtk
```

# Install nvidia 
## using .run
Make sure you are logged out.

Hit `CTRL+ALT+F1` and login using your credentials.

kill your current X server session by typing `sudo service lightdm stop` or `sudo lightdm stop`

Enter runlevel 3 by typing `sudo init 3` and install your *.run file.

You might be required to reboot when the installation finishes. If not, run `sudo service lightdm start` or `sudo start lightdm` to start your X server again.

## using apt
```
sudo add-apt-repository ppa:ubuntu-x-swat/x-updates
sudo apt-get update
sudo apt-get install nvidia-current
```

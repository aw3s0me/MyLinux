# MyLinux

##Packages
###Multi-tab terminal

```shell
sudo apt-get install xdotool
```

ctrl+shift+t - open new tab
###JDK-JRE
```shell
sudo apt-get install default-jre
sudo apt-get install default-jdk
```
Get the jre path using
```shell
sudo update-alternatives --config java
```
Insert to this file to the end as: JAVA_HOME="/usr/lib/jvm/java-8-oracle"
```shell
sudo nano /etc/environment
```
Save, exit and reload using:
```shell
source /etc/environment
```

###Copying to clipboard
```shell
sudo apt-get install xsel
xsel --clipboard < new-clipboard-contents.txt
xsel --clipboard > current-clipboard-contents.txt
```

###Unzip
```
sudo apt-get install unzip
unzip file.zip -d destination_folder
```

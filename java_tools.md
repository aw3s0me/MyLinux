# Java status process tool (to check running jar files or find their ids)
```
jps -m
```
## Print just id and class name (more convenient and concise)
```
jps -lV
```

# Installing JDK-JRE
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

# Installing Intellij
Download idea.tar.gz

```
sudo tar xf idea.tar.gz -C /opt/
cd /opt/idea/bin
./idea.sh
```

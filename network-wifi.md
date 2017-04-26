# Solving 17.04 Ubuntu error 
Check `cat /etc/resolv.conf` for your DNS settings

And add following name server in ``sudo nano /etc/resolvconf/resolv.conf.d/base`:
```
nameserver 8.8.8.8
nameserver 8.8.4.4
```
Add the same to `sudo nano /etc/resolvconf/resolv.conf.d/head`:
```
nameserver 8.8.8.8
nameserver 8.8.4.4
```
Update resolconf:
```
sudo resolvconf -u
```
Check updates 
```
cat /etc/resolv.conf
```

# DNS
## Install testing util for ubuntu
```
sudo apt install ldnsutils
```
## Testing dns
```
drill <address>
drill google.com
```

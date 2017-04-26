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
Right order must be:
```
nameserver 127.0.0.53
nameserver 8.8.8.8
nameserver 8.8.4.4
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

# ifconfig
## View all network setting
```
ifconfig
```
## Display info of all network interfaces
```
ifconfig -a
```
## Display info about specific interface
```
ifconfig <interface_name>
(e.g.) ifconfig eth0
```
## Enabling (switching on) an network interface
```
ifconfig eth0 up
or
ifup eth0
```
## Disabling (switching off) an network interface
```
ifconfig eth0 down
or
ifdown eth0
```
## Assign a ip address to network interface
```
ifconfig eth0 172.16.25.125
```
## Assign netmask to network interface
```
ifconfig eth0 255.255.255.224
```
## How to assign a broadcast to network interface
```
ifconfig eth0 broadcast 172.16.25.63
```
## Assign IP Netmask + Broadcast to network interface
```
ifconfig eth0 172.16.25.125 netmask 255.255.255.224 broadcast 172.16.25.63
```
## Assign limit size of packets transmitted on interface (MTU)
```
ifconfig <interface> mtu <max num of octets in one transaction>
ifconfig eth0 mtu 1000
```
## Enable promiscuous mode
In this mode interface accepts all packets without checking whether it belongs to interface
```
ifconfig eth0 promisc #enable
ifconfig eth0 -promisc #disable
```
## Change MAC of network interface
```
ifconfig eth0 hw ether <MAC>
```


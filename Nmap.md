# Problem: 
```
$ nmap --privileged -sS $IP           
Starting Nmap 7.97 ( https://nmap.org )
Couldn't open a raw socket. Error: Operation not permitted (1)
```
# Solution: (nmap needs the cap_net_raw capability to do most of the scan types without being root)
```
sudo setcap -r /usr/bin/nmap ; sudo setcap cap_net_raw+ep /usr/bin/nmap
```

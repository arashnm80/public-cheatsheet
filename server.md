- find all occupied ports: `netstat -plnt`
- create socks proxy on server with dante:
```
https://www.digitalocean.com/community/tutorials/how-to-set-up-dante-proxy-on-ubuntu-20-04
```
- SSH Key-Based Authentication
```
https://www.youtube.com/watch?v=vpk_1gldOAE
```
- keep ssh tunnel alive
```
ssh -o ServerAliveInterval=600 username@server_ip_address
```
- bash script to always run ssh tunnel and keep it alive (public and private key set should be established before)
```
#!/bin/bash

# if not found - equals to 1, start it
while true
do
    ps -ef | grep USER@SERVER-IP | grep -v grep
    if [ $? -eq 1 ]
    then
        /usr/bin/ssh -NfqD 1080 -o ServerAliveInterval=200 USER@SERVER-IP
    else
        echo "ssh-tunnel.sh is running"
    fi
    sleep 30
done
```
- add floating ip to server
```
sudo ip addr add XXX.XXX.XXX.XXX dev eth0
```
- check or delete ip from previous command:
```
sudo ip addr show
sudo ip addr del XXX.XXX.XXX.XXX dev eth0
```
- ssh with middle server
```
ssh -J <middle-user>:<middle-ip> <user>:<ip>
```

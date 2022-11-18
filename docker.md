### Forcefully Remove Containers and Images
1. remove all docker containers:
```
sudo docker rm -f $(sudo docker ps -qa)
```
2. remove all docker images:
```
sudo docker rmi -f $(sudo docker images -aq)
```
3. install docker
```
curl -fsSL https://get.docker.com | sh
```
4. downloading-docker-image-for-transfer-to-non-internet-connected-machine
```
https://serverfault.com/questions/701248/downloading-docker-image-for-transfer-to-non-internet-connected-machine
or
https://stackoverflow.com/questions/48125169/how-run-docker-images-without-connect-to-internet
```

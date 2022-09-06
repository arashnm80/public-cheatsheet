### Forcefully Remove Containers and Images
1. remove all docker containers:
```
sudo docker rm -f $(sudo docker ps -qa)
```
2. remove all docker images:
```
sudo docker rmi -f $(sudo docker images -aq)
```

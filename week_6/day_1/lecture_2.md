# lecture 2 (10:30 - 12:00)

## docker installation

for linux
+ https://get.docker.com/
  
for windows 
+ docker desktop


to check if docker installed successfully use this command.
``` console
$ docekr info
```
docker daemon config file path `/etc/docker/daemon.json`.


we can change or add or remove remove registry from daemon config file.

``` json
{

    ...
    "registry-mirrors" : ["https://hub.hamdock.ir"]
}
```
we can change or add or remove remove registry from daemon config file.


file for docker service config `etc/systemd/docker.service.d/test.conf`.

after changing docker service config
``` console 
$ systemctl daemon-reload

```

+ todo: complete above commands


### volumes 


### 
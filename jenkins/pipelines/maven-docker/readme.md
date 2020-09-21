# Docker with Jenkins - Docker Container

### Installation

Create jenkins_home folder
```sh
$ mkdir jenkins_home
```

Up Jenkins Container
```sh
$ docker-compose up -d
$ docker-compose build && docker-compose up -d
```
Verify the deployment by navigating to your server address in your preferred browser.

```sh
127.0.0.1:9000
```

Down Jenkins Container
```sh
$ docker compose down
```

Get password
```sh
$ cat jenkins_home/secrets/initialAdminPassword
```

Get password
```sh
$ docker exec -it jenkins /bin/bash
cat /var/jenkins_home/secrets/initialAdminPassword
```

### Test Docker
List containers
```sh
$ docker exec -it jenkins /bin/bash
$ docker ps
```
###### ERROR
<< Got permission denied while trying to connect to the Docker daemon socket at unix:///var/run/docker.sock >>

```sh
$ docker exec -it -u root jenkins /bin/bash
$ chown jenkins /var/run/docker.sock
```
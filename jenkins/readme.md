# Jenkins - Docker

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
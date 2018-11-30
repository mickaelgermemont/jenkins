# Jenkins

https://hub.docker.com/r/jenkins/jenkins/tags/

# Run

```
docker run --rm --name jenkins1 -p 8080:8080 -p 50000:50000 --mount type=volume,src=Jenkins,dst=/var/jenkins_home jenkins/jenkins:2.151-slim

open http://localhost:8080/
```

user is : mickael
password is : mickael

# Backup

If your volume is inside a container - you can use the following command to extract the data.

```
docker cp jenkins1:/var/jenkins_home .
```

# troubleshoot

```
docker exec -it jenkins1 /bin/bash
```

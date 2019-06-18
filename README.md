## Jenkins

This repository contains the Dockerfile to create a Jenkin's master image.

It contains the Jenkins itself and the CodeClimate cli, the latter is used to send the coverage report to the CodeClimate.

The image is already published on Docker hub, if you want to make some changes to it, you have to rebuild it and to republished it to the Docker hub:

```bash
docker build -t asseinfo/jenkins .
docker push asseinfo/jenkins
```

### How to start the Jenkins container

Run the below command to start the Jenkins container:

```bash
docker run -d -u root --name jenkins_master --restart always -p 8080:8080 -p 50000:50000 -v /var/jenkins_home:/var/jenkins_home -v /var/run/docker.sock:/var/run/docker.sock asseinfo/jenkins
```

### Docker hub images

https://hub.docker.com/r/asseinfo

Run the below command to start the Jenkins container:

```bash
docker run -u root --restart always -p 8080:8080 -p 50000:50000 -v /var/jenkins_home:/var/jenkins_home -v /var/run/docker.sock:/var/run/docker.sock asseinfo/jenkins
```

### Docker hub image

https://hub.docker.com/r/asseinfo/jenkins

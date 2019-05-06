## Master

Run the below command to start the Jenkins container:

```bash
docker run -u root --name jenkins_master --restart always -p 8080:8080 -p 50000:50000 -v /var/jenkins_home:/var/jenkins_home -v /var/run/docker.sock:/var/run/docker.sock -v $HOME/.ssh:/root/.ssh asseinfo/jenkins
```

## Slaves

Configure the below command in **Launch agent via execution of command on the master**:

```bash
ssh -o StrictHostKeyChecking=no [user]@[host] docker run -i --rm --name agent --init asseinfo/jenkins-slave
```

after setting Remote root directory to `/home/jenkins/agent`.


### Docker hub images

https://hub.docker.com/r/asseinfo

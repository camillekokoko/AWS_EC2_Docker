# AWS_EC2_Docker

## Overview: AWS Framework

<p align="center">
  <img src="https://raw.githubusercontent.com/camillekokoko/AWS_EC2_Docker/main/AWS_framework.jpeg" alt="AWS Framework" width="500">
</p>

**1.** Go to aws
```
 sudo
```

**4.** Installing Docker on OS Image (Ubuntu)
```
sudo apt install docker.io
```

**5.** Install all the dependency packages 
```
sudo snap install docker
```

**6.** (Optional) Check the version
```
docker --version
```

**7.** Pull an image from Docker hub. "Run" is for interactive mode. "Start" is running it in the background.
```
# Pull and run the nginx image
sudo docker run <image>

# If the container is stopped, you can start it again
sudo docker start <image>
```

**8.** (Optional) Check all the containers pulled
```
docker --version
```

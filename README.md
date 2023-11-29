# AWS EC2 Instance Setup with Docker

## Overview: AWS Framework

<p align="center">
  <img src="https://raw.githubusercontent.com/camillekokoko/AWS_EC2_Docker/main/AWS_framework.jpeg" alt="AWS Framework" width="500">
</p>

## AWS Cloud and EC2 instance Setup

**1.** 
Navigate to AWS EC2 and initiate the instance launch process.
**2.** 
Select the desired operating system image, such as Ubuntu, macOS, or Windows. 
**3.** 
Select an instance type (CPU/memory) for instance free tier.
**4.** 
Configure a security group to manage the instance's traffic and enhance its security settings.


## Docker Setup

**1.** Installing Docker on OS Image (Ubuntu)
```
sudo apt install docker.io
```

**2.** Install dependency packages 
```
sudo snap install docker
```

**3.** (Optional) Check the version
```
docker --version
```

**4.** Pull an image from [Docker hub](https://hub.docker.com/). "Run" is for interactive mode. "Start" is running in the background.
```
# Pull and run the nginx image
sudo docker run <image>

# If the container is stopped, you can start it again
sudo docker start <image>
```

**5.** (Optional) Check all the containers pulled
```
sudo docker images
```

**6.** (Optional) Check if containers are running
```
sudo docker ps
```

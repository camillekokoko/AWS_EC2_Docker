# AWS EC2 Instance Setup with Docker

## Overview: AWS Framework

<p align="center">
  <img src="https://raw.githubusercontent.com/camillekokoko/AWS_EC2_Docker/main/AWS_framework.jpeg" alt="AWS Framework" width="500">
</p>

## AWS Cloud and EC2 instance Setup
1. **Instance Launch on AWS EC2:**
   Navigate to [AWS EC2](https://aws.amazon.com/) and initiate the instance launch process.

2. **Operating System Selection:**
   Select the desired operating system image, such as Ubuntu, macOS, or Windows.

3. **Instance Type (Free Tier):**
   Choose an instance type based on CPU and memory requirements eligible for the [free tier](https://aws.amazon.com/free/?gclid=Cj0KCQiA35urBhDCARIsAOU7QwkBj6iXTdem4fRN2bKDH8qkG2fG5aOWDSjTXI6etVCLz_WEK_D4gKYaAgEtEALw_wcB&all-free-tier.sort-by=item.additionalFields.SortRank&all-free-tier.sort-order=asc&awsf.Free%20Tier%20Types=*all&awsf.Free%20Tier%20Categories=categories%23compute&trk=5136fcc7-fda9-45d9-a722-6e7f07f8bafa&sc_channel=ps&ef_id=Cj0KCQiA35urBhDCARIsAOU7QwkBj6iXTdem4fRN2bKDH8qkG2fG5aOWDSjTXI6etVCLz_WEK_D4gKYaAgEtEALw_wcB:G:s&s_kwcid=AL!4422!3!476956951563!e!!g!!aws%20cloud!11539887573!114142395562).

4. **Security Group Configuration:**
   Configure a security group to manage the instance's traffic and enhance its security settings.

5. **Launch the instance and download the private key file**

## Git Setup
**1.** Connect to EC2 instance
```
ssh -i your-key.pem ubuntu@your-ec2-instance-ip
```
**2.** (Optional) Update the package manager
```
sudo apt update
```
**3.** Install Git
```
sudo apt install git -y
```
**4.** (Optional) Check Git version
```
git --version
```

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

## Clone the Repository of the Application
```
git clone <repo>
```
## Configuring and Running the Dockerized Application
```
# Build and start the containers using Docker Compose
docker-compose up --build
```
## Configuring AWS Security Group
1. **Go to the AWS Management Console and navigate to the EC2 service.**
2. **Select running instance and click on "Actions" > "Networking" > "Change Security Groups."**
3. **Create a new security group or modify the existing one.**
4. **Add a new inbound rule to allow traffic on port 3001 (or the desired port) from anywhere (0.0.0.0/0).**

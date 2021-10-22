#simple_web
A simple web server that outputs the IP addresses of the source and destination, very useful for testing loadbalancer to show real requests.

Supported tags and respective Dockerfile links
latest (latest/Dockerfile)
For more information about this image and its history, please see the relevant manifest file in the yeasy/simple-web GitHub repo.

What is simple-web?
simple-web is a simple web to show the source and destination IP addresses of the received requests information, written in python.

How to use this image?
The docker image is auto built at https://registry.hub.docker.com/u/yeasy/simple-web/.

In Dockerfile
FROM yeasy/simple-web:latest
Local Run
$ docker run --rm -it -p 80:80 yeasy/simple-web:latest
Which image is based on?
The image is based on python:2.7

What has been changed?
Add the index.py code.

Supported Docker versions
This image is officially supported on Docker version 1.7.1.

Support for older versions (down to 1.0) is provided on a best-effort basis.

User Feedback
Documentation
Be sure to familiarize yourself with the repository's README.md file before attempting a pull request.

Issues
If you have any problems with or questions about this image, please contact us through a GitHub issue.

You can also reach many of the official image maintainers via the email.

Contributing
You are invited to contribute new features, fixes, or updates, large or small; we are always thrilled to receive pull requests, and do our best to process them as fast as we can.

Before you start to code, we recommend discussing your plans through a GitHub issue, especially for more ambitious contributions. This gives other contributors a chance to point you in the right direction, give you feedback on your design, and help you find out if someone else is working on the same thing.


Project we are going to build 


![1_lQRMlhViPuNOa22RmE8aXw](https://user-images.githubusercontent.com/41754537/135728164-89837e1c-7eb2-4ebd-9985-416ff3663369.png)

Prerequisites

Ec2-Instance-Any Linux OS

Python — a prerequisite for the AWS CLI

PIP — a prerequisite for the AWS CLI

Install AWS CLI

jq — a command line utility for parsing JSON output

Install Git : yum install git -y

Install Docker :

yum install docker -y 

 service docker start
 
 usermod -aG docker jenkins
  
Install Jenkins

sudo wget -O /etc/yum.repos.d/jenkins.repo http://pkg.jenkins-ci.org/redhat-stab

sudo rpm --import https://jenkins-ci.org/redhat/jenkins

sudo yum install jenkins -y

sudo service jenkins start

Create an ECR Registry

![image](https://user-images.githubusercontent.com/41754537/135728681-9b8e611b-03fb-4c1c-a2d0-0fa84a0d4380.png)

Create an ECS Cluster :

![image](https://user-images.githubusercontent.com/41754537/135728708-ddf1b4de-c99c-4323-ad8d-d722ad7ce711.png)

We have to provide the Ec2 machine with Roles as below :

https://docs.amazonaws.cn/en_us/AmazonECS/latest/developerguide/task_execution_IAM_role.html

Steps as Below :

the project should be cloned to your workspace ,so enable your repo so jenkins is notified when files are pushed 

create a pipeline project and simple copy jenkinsfile or use scm 

![image](https://user-images.githubusercontent.com/41754537/135729168-e9c6758e-58b5-4016-ad7f-b5a1e5781cd4.png)

The pipeline stahe view is following:

![image](https://user-images.githubusercontent.com/41754537/135729412-c48ab715-7f36-416e-b0e2-b5d41003e4ba.png)

Clone the project and replace the ECR Repo,Cluster Name,Repository Name as your wish and run the jenkis Job:

![image](https://user-images.githubusercontent.com/41754537/135729522-8a06a996-7941-49b4-8188-545de6cbb42f.png)

![image](https://user-images.githubusercontent.com/41754537/135729535-9d067387-9810-4861-8c3d-45ce9592e00b.png)

![image](https://user-images.githubusercontent.com/41754537/135729571-bec7ce71-0279-418f-badf-8d269b33363f.png)

![image](https://user-images.githubusercontent.com/41754537/135729586-675af1ff-6e58-42b7-a472-35717ed15cf4.png)


























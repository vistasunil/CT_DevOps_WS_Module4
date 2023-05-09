<div align="center">
<img src=https://static.wixstatic.com/media/1c706c_a5df0ad56f894928bf858a74ba744b32~mv2.png/v1/fit/w_2500,h_1330,al_c/1c706c_a5df0ad56f894928bf858a74ba744b32~mv2.png width="400" height="200">
 </div>

# <div align="center"> DOCKER RUNBOOK </p>

# <div align="center"> DevOps Instructor-led Training </div>

<br />

<br />

<br />

<br />

# $${\color{brown} &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; Contact us: &emsp;&emsp;&emsp; }$$

<div align="right"> T O A C C E L E R A T E Y O U R C A R E E R G R O W T H </div>

### <div align="right"> For questions and more details: </div>

<div align="right"> <img src=https://w7.pngwing.com/pngs/759/922/png-transparent-telephone-logo-iphone-telephone-call-smartphone-phone-electronics-text-trademark-thumbnail.png width="20" height="20"> +91 98712 72900 </div>

<div align="right"> <img src=https://pbs.twimg.com/profile_images/1450734615946219520/jmBHQRRa_400x400.jpg width="20" height="20"> https://www.thecloudtrain.com </div>

<div align="right"> <img src=https://icons.iconarchive.com/icons/martz90/circle/512/email-icon.png width="20" height="20"> support@thecloudtrain.com </div>

<div align="right"> <img src=https://png.pngtree.com/png-vector/20221018/ourmid/pngtree-whatsapp-icon-png-image_6315990.png width="20" height="20"> +91 98712 72900 </div>

## _Find solutions to your assingment below:_

## Exercise 1: Accomplish below task to complete this exercise:**

a) Install docker on an Ubuntu GCP instance

### _Solution:_

Refer [Official Docker installation page](https://docs.docker.com/engine/install/ubuntu/) for installation steps.

**Post installation steps**

i. Add your current user to docker group to allow access on docker commands:

`sudo usermod -a -G docker $USER`

ii. Logout from terminal and login to the user again

`exit`

b) Use docker pull to download docker images on this server

### _Solution:_

`docker pull nginx`

![image](https://github.com/vistasunil/CT_DevOps_WS_Module4/assets/37858762/54f46d2b-125e-4844-9c5c-9daad8ddca3c)

c) Use docker run to run nginx container using this image. Use below parameters for the container
  i. Name: ' **mynginx'**
  ii. Host port: 80
  iii. Container port: 80
  iv. Should run in detach mode

### _Solution:_

`docker run -ti -d --name mynginx -p 80:80 nginx`

![image](https://github.com/vistasunil/CT_DevOps_WS_Module4/assets/37858762/b374a5f1-7147-4575-9b24-9c470a3ba090)

d) Login to mynginx container and check the nginx process running or not. Ideally it should be running:

### _Solution:_

`docker exec -ti mynginx bash`

Install procps to run ps command inside container

![image](https://github.com/vistasunil/CT_DevOps_WS_Module4/assets/37858762/d7e630c5-4a55-4b5e-a284-93c03ea3f40d)

e) Check if nginx is accessible on _**http://<Server\_Pubilc\_IP\>:80**_ and you see below page:

![image](https://github.com/vistasunil/CT_DevOps_WS_Module4/assets/37858762/8fa87c71-63a0-4834-a445-048cdf03c737)

## Exercise 2: Accomplish below task to complete this exercise:**

a) Create a Dockerfile to package below:
  i. uses ubuntu docker image
  ii. Install apache2 inside it
  iii. Mount any local html file from host to /var/www/html path of container
  iv. Uses command as entrypoint: `ENTRYPOINT apachectl -D FOREGROUND`

### _Solution:_

a) First, create a folder docker, in the home directory

```
mkdir docker
cd docker
```

![image](https://github.com/vistasunil/CT_DevOps_WS_Module4/assets/37858762/8e1c71a0-6e8a-49bb-80dd-b0fcac05cae0)

Enter into this directory, and create a file called 'Dockerfile', with the same contents as the Sample Dockerfile. Add the following content in the Dockerfile.

`sudo vim Dockerfile`

Add the below content in Dockerfile

```
FROM ubuntu
ENV TZ=Asia/Kolkata
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ \> /etc/timezone
RUN apt-get update
RUN apt-get -y install apache2
ADD . /var/www/html
ENTRYPOINT apachectl -D FOREGROUND
ENV name Devops Tutorial
```

![image](https://github.com/vistasunil/CT_DevOps_WS_Module4/assets/37858762/75b6b9b7-f13e-49a3-95de-affe21721817)

b) Create a sample html file with some content in the same directory as Dockerfile

### _Solution:_

Create one more file called, index.html with the following contents can verify the push on DockerHub.

`sudo vim index.html`

Add the below content in html file

```
<html>
<title> Sample Website </title>
<body>
  Hello World
</body>
</html>
```

![image](https://github.com/vistasunil/CT_DevOps_WS_Module4/assets/37858762/60ecb4b9-0294-4760-94de-9a692e0457a9)

c) Once above Dockerfile is ready, perform below tasks:
  i. Build the dockerfile with name **ubuntu\_apache**

### _Solution:_

`docker build <directory-of-dockerfile> -t <name of image>`

![image](https://github.com/vistasunil/CT_DevOps_WS_Module4/assets/37858762/1209946c-817c-4d41-831c-a679e5b70acf)

![image](https://github.com/vistasunil/CT_DevOps_WS_Module4/assets/37858762/01f9f4b9-74fd-487f-ac26-0e59467869fb)

  ii. Spawn a new container using below params:
    * Name: **myapache**
    * Host port: 81
    * Container port: 80
    * Should run in detach mode

### _Solution:_

Run this built image, using the following command:

`docker run –it –name myapache –p 81:80 –d <name of image>`

![image](https://github.com/vistasunil/CT_DevOps_WS_Module4/assets/37858762/d195d2dd-eaca-4e49-ad22-321f8c80c4cc)

  iii. Check if apache is accessible on **_http://\<Server\_Pubilc\_IP\>:81_** and you see the content of html file you created in step **b**.

### _Solution:_

Navigate to the server IP address on port 81

_ **Note:** Make sure port 81 is open on the server using firewall rule_

![image](https://github.com/vistasunil/CT_DevOps_WS_Module4/assets/37858762/42d7ca3e-e04e-4c70-b595-4f011503f742)

Finally, login into the container, and check the variable $name, it will have the same value, as given in the Dockerfile.

![image](https://github.com/vistasunil/CT_DevOps_WS_Module4/assets/37858762/9f5047c6-9e6f-43bf-bfca-c885bb21c25d)

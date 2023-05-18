<div align="center">
<img src=https://static.wixstatic.com/media/1c706c_a5df0ad56f894928bf858a74ba744b32~mv2.png/v1/fit/w_2500,h_1330,al_c/1c706c_a5df0ad56f894928bf858a74ba744b32~mv2.png width="400" height="200">
 </div>

# <div align="center"> DOCKER ASSIGNMENT </p>

# <div align="center"> DevOps Workshop Training </div>

# <div align="right"> $`\textcolor{brown}{\text{Contact us: }}`$  &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; </div>

<div align="right"> T O A C C E L E R A T E Y O U R C A R E E R G R O W T H </div>

### <div align="right"> For questions and more details: </div>

<div align="right"> <img src=https://w7.pngwing.com/pngs/759/922/png-transparent-telephone-logo-iphone-telephone-call-smartphone-phone-electronics-text-trademark-thumbnail.png width="20" height="20"> +91 98712 72900 </div>

<div align="right"> <img src=https://pbs.twimg.com/profile_images/1450734615946219520/jmBHQRRa_400x400.jpg width="20" height="20"> https://www.thecloudtrain.com </div>

<div align="right"> <img src=https://icons.iconarchive.com/icons/martz90/circle/512/email-icon.png width="20" height="20"> support@thecloudtrain.com </div>

<div align="right"> <img src=https://png.pngtree.com/png-vector/20221018/ourmid/pngtree-whatsapp-icon-png-image_6315990.png width="20" height="20"> +91 98712 72900 </div>

#
</br>

## $`\textcolor{red}{\text{NOTE: USE UBUNTU 22.04 VIRTUAL MACHINES FOR ALL THE LABS}}`$

## _Complete below exercises:_

## Exercise 1: Accomplish below task to complete this exercise:

a) Install docker on an Ubuntu GCP instance

b) Use docker pull to download docker images on this server

c) Use docker run to run nginx container using this image. Use below parameters for the container

  - i. Name: **mynginx**
  
  - ii. Host port: 80
  
  - iii. Container port: 80
  
  - iv. Should run in detach mode
  
d) Login to mynginx container and check the nginx process running or not. Ideally it should be running

e) Check if nginx is accessible on **_http://\<Server\_Pubilc\_IP\>:80_** and you see below page:

![image](https://github.com/vistasunil/CT_DevOps_WS_Module4/assets/37858762/1ca7b0b7-b76f-44af-b75a-64a5978659ca)

## Exercise 2: Accomplish below task to complete this exercise:

a) Create a Dockerfile to package below:

  - i. uses ubuntu docker image
  
  - ii. Install apache2 inside it
  
  - iii. Mount any local html file from host to /var/www/html path of container
  
  - iv. Uses command as entrypoint: `ENTRYPOINT apachectl -D FOREGROUND`

b) Create a sample html file with some content in the same directory as dockerfile

c) Once above Dockerfile is ready, perform below tasks:

  - i. Build the dockerfile with name **ubuntu_apache**
  
  - ii. Spawn a new container using below params:
  
    * Name: ' **myapache'**
    * Host port: 81
    * Container port: 80
    * Should run in detach mode
	
  - iii. Check if apache is accessible on http://\<Server\_Pubilc\_IP\>:81 and you see the content of html file you created in step **'b'.**


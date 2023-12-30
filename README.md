# Docker-Image
In this project I have tried to create a <b>Docker Image</b> of a simple html page, push the image to docker hub as well as pull the image from docker hub for later use.

<h1>Process</h1>
First I created a directory named <b>dockerhtml</b> and created a simple html file <b>index.html</b> to try it on my local machine. Then I built the docker with the command <b>"docker build -t dockerhtml . "</b> <br><br>

![docker2](https://github.com/prasannashah1/Docker-Image/assets/28432698/7742a688-7a42-429e-a46e-20e6d4c017f0) <br>
Now you can list the image with <b>"docker images"</b> command. <br><br>
Run the image with <b>"docker run -dit -p 8080:80 --name dockerhmtl dockerhtml"</b> command. <br><br>
The html page will be available at <b>"http://ip:8080"</b> <br>

![docker7](https://github.com/prasannashah1/Docker-Image/assets/28432698/fda03838-6ffe-421d-8c3b-4b07613ff6b8) <br>
You can also list the running container with <b>"docker ps"</b> command.<br>

![docker6](https://github.com/prasannashah1/Docker-Image/assets/28432698/0489c853-a623-440d-8120-9e62c819ca2f) <br>
<h2>Pushing Docker Image to Docker Hub</h2>
Create a file namd <b>'Dockerfile'</b> inside the <b>dockerhtml</b> directory, staying inside the directory write the following command to the file and save the file.<br><br>

 <b>FROM httpd</b><br>
 <b>COPY . /usr/local/apache2/htdocs/</b><br>

  Tag the image to the docker hub account with <b>"docker tag dockerhtml pr45an94/dockerhtml:latest"</b> command and list the tagged docker image.
 
 ![docker8](https://github.com/prasannashah1/Docker-Image/assets/28432698/2ae66af9-1369-4f13-8617-e80a40222e6f) <br>

 Login to the docker hub with the command <b>"docker login"</b>. Enter the username and password of the docker hub account.<br>
 
![docker9](https://github.com/prasannashah1/Docker-Image/assets/28432698/a72a03c9-7a77-444d-9522-b7d642881b05) <br>

Push the tagged docker image to docker hub account with <b>"docker push pr45an94/dockerhtml:latest"</b> command <br>

![docker11](https://github.com/prasannashah1/Docker-Image/assets/28432698/acf4af5e-90df-4845-abdd-0f8d0aa880d8) <br>

You can see that the docker image has been uploaded to your docker hub repository.<br>

![docker12](https://github.com/prasannashah1/Docker-Image/assets/28432698/868acdec-2f04-46e6-9189-71e9511e23dc) <br>

Now you can remove the image from you local machine and pull the image from docker hub repository. <br>

![docker13](https://github.com/prasannashah1/Docker-Image/assets/28432698/8f431d63-58b1-4765-95b6-a54622361c02)<br>

![docker14](https://github.com/prasannashah1/Docker-Image/assets/28432698/5aee8d9a-dc1d-451e-91b2-05a8da90f8e1) <br>

![docker15](https://github.com/prasannashah1/Docker-Image/assets/28432698/037d799e-fe8f-4552-a1a2-709699cf6fbe) <br>

<h2>Conclusion</h2>
This is a simple Docker project that shows how to create your own Docker Image and push it to Docker Hub Repository.








 

 


 






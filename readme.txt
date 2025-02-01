#Task2 Linux
Running on WSL Ubuntu server

mkdir VettyTest #create Dir
cd VettyTest
touch scipt.sh #create shell script
vi script.sh

#----contents
#!/bin/bash
echo "Welcome to DevOps!"
#-----------------------------------

chmod +x script.sh #creating executable 
./script.sh  #running 

prints Welcome to Devops to terminal


#Task 3
#Docker 

Running on WSL ubuntu server

mkdir dock-nginx

touch Dockerfile  #creating Dockerfile containing instruction

#--contents

FROM nginx:Latest     #fetches the latest nginx base image
EXPOSE 80    #app listens on port 80 in the container
CMD ["nginx", "-g", "daemon off;"]  

#----contents

docker build -t self-nginx .   #building the image from the Docker file present i:n the root directory 
docker images   #lists all iamges
docker run -d -p 8080:80 --name nginx-container self-nginx  #runs container on port 80 (maps host port 8080 to 80 port inside container)
docker ps  #shows running containers to check if my container nginx-container running or not

now visit localhost:8080 youll find the nginx default page opened


Thank YOU

Hrithik Besra




















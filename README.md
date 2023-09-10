# learn-docker

docker login  
docker push

***Container Commands -***   
docker run nginx - Runs a container in an attached mode  
docker run ubuntu - Runs and exits the container  
docker run ubuntu sleep 5 - Runs and sleep for 5s. After 5s container stops  
docker run -d nginx - Runs the container in detached mode in the background  
docker attach <container_id> - Attach to an already running container  
docker ps - List all running containers. Basic info about container  
docker ps -a - Lists all running, stopped and exited containers  
docker stop <container name/id> - Stops a running container  
docker rm <container name/id> - Removes a stopped/exited container permanently  
docker exec <container name> cat etc/hosts - List content of host file inside a container  


***Image Commands -***   
docker images - Lists available images and their sizes  
docker rmi nginx - Removed the image  
docker pull nginx - Pulls only image. Doesn’t execute a container  


***Docker run -***    
docker run -it nginx - interactive and terminal option  


**Run -Port mapping - Port Mapping/Publishing on containers -**   
docker run -p 80:5000 nginx 
docker run -p 8080:8080 jenkins/jenkins - runs a new container every time

**Run -Volume mapping -**   
For persisting data map a directory outside container in docker host  
docker run -p 8080:8080 jenkins/jenkins - runs a new container every time  

***Inspect Container -***   
docker inspect <container_name> - Detailed info about container  


***Container Logs -***   
docker logs <container id/name>  



***Advanced Docker commands -***   
Tags for image versioning  

***Attached/Detached mode -***   
docker run -d ubuntu sleep 1500 - Runs container in background  
docker attach <container_id> - run container in foreground  



***Create own image and run -***   
docker build <dockerfile_name>  
docker  build . -t <image_name> - Builds an image using a docker file and gives it the tag <image_name>  



***Environment Variables -***   
docker inspect <container_name> - List env variables configured for the container  
docker run -e <env_var>=<value> <image_name>  


***Command vs Entrypoint - Explore***  
CMD nginx  
docker run --entrypoint - explore more  



***Docker Compose -***   
docker-compose.yaml  
docker-compose up - Brings up entire application stack  

docker run --name=name <image_name> - Gives a name to the container to be linked  
docker run --link - links more than one running containers by name  
docker compose - build  
docker compose - versions  







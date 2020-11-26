### Docker Run Command
``sudo docker run docker/whalesay cowsay Mert Köprücü``

### Docker List All Containers
``docker ps -a``

### Stop a container name
``docker stop <container_name/id>``

### Remove contaier permanently
``docker rm <container_name/id>``

After this command, ``docker ps -a`` doesn't show removed containers.

### List all installed images
``docker images``

### To remove image
``docker rmi <image_name>``

- Delete all dependent containers to remove image

### Download an image and name it
``docker run --name webapp nginx:1.14-alpine``

### Only download image don't run it
``docker pull <image_name>``

### Docker pull by digest (It is secure to be protected from unintentionally image changes.)
``docker pull alpine@sha256:4e01ddea8def856ba9fee17668fa0b2e45a8bc78127b7ab6cf921f6d6fd86ac9``

### Execute command
``docker exec <image_name> cat /etc/hosts``

### Detach a container
``docker run -d <image_name>``

### Attach a container to see output 
``docker attach <container_id>``

### Interactive Mode
``docker run -it kodekloud/simple-prompt-docker``

### Port mapping
``docker run -p 8080:8080 kodekloud/simple-webapp``

### Volume mapping
``docker run -v /opt/mysql:/var/lib/mysql mysql``

### Inspect container
``docker inspect <container_name>``

``docker inspect <container_name> | grep IPAddress``

### Container logs
``docker logs <container_id>``

### Environment Variables
``docker run -e APP_COLOR=blue simple-webapp-color``

### Inspect Environment Variables
``docker inspect <container_id>``

You can see environment variables under ``ENV`` tag of json output.

### Run Docker without sudo

``sudo usermod -aG docker ${USER}``
``su - ${USER}``

### Docker easy installation for ubuntu

``wget -qO- https://get.docker.com | sh``

### Docker cp command

``docker inspect redis-konteyner | grep IPAddress``



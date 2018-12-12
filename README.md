# Dockerfiles
Repository to hold various Dockerfiles for images I create.

# How to publish to Docker Hub (steps to remind me)

### Build the docker image locally from the Dockerfile

```console
docker build -t my_local_image .
```

### Make sure the image is listed
```console
docker images
```
### Should show the docker image with the name `my_local_image`

### Run the image on local machine to make sure it will run successfully (remember port forwarding)
```console
docker run -p local_machine_port:docker_image_port my_local_image
```

### Publish to Docker Hub
```console
docker login
```
### Follow prompts with login/password

### (OPTIONAL) Tag image
```console
docker tag my_local_image siliconrob/dockerfiles:tag
```

### Push image to Docker Hub
```console
docker tag my_local_image siliconrob/dockerfiles:tag
```

### (VERIFICATION) Download your published image from Docker Hub
```console
docker pull siliconrob/dockerfiles:tag
```

### (VERIFICATION RUN) Run the Docker Hub pulled image locally
```console
docker run -it siliconrob/dockerfiles:tag
```

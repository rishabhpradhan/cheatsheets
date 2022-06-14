### Docker cheatsheet


#### Build
Build an image from the Dockerfile in thecurrent directory and tag the image </br>
`docker build -t myimage:1.0 .`

List all images that are locally stored withthe Docker Engine </br>
`docker image ls`

Delete an image from the local image store </br>
`docker image rm alpine:3.4`


Start a new CONTAINER from IMAGE </br>
`docker run IMAGE` </br>
`docker run ngix`
</br>

#### Run
Run a container from the Alpine version 3.9 image, name the running container “web” and expose port 5000 externally,mapped to port 80 inside the container </br>
`docker container run --name web -p 5000:80 alpine:3.9`

Stop a running container through SIGTERM </br>
`docker container stop web`

Stop a running container through SIGKILL </br>
`docker container kill web`

List the networks  </br>
`docker network ls`

List the running containers (add --all to include stopped containers)  </br>
`docker container ls`

Delete all running and stopped containers </br>
`docker container rm -f $(docker ps -aq)`
</br>

#### Share
Pull an image from a registry </br>
`docker pull myimage:1.0`

Retag a local image with a new image name and tag </br>
`docker tag myimage:1.0 myrepo/myimage:2.0`

Push an image to a registry </br>
`docker push myrepo/myimage:2.0 `
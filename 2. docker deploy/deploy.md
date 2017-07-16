### Delete all containers
> docker rm $(docker ps -a -q)

### Delete all images
> docker rmi $(docker images -q)

### build the image to docker and deploy rancher/docker hub:

#### build docker first (do not forget the . at the end)
* docker build -t (tagId) . 
* docker run -d -p (accessPort/InternalPort) tagId

#### deply docker image
* docker login (docker repository hub)
* docker images (find the image id)
* docker tag f76fe6c9888a (imageid) (docker repository hub)
* docker push (docker repository hub)

#### then setup the rancher environment to pull the images


 


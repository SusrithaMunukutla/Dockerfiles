# Dockerfiles

	Procedure to build an image out of a Dockerfile is as follows:
-	Create new directory $ mkdir directory_name
-	Change into that directory $ cd directory_name
-	Create a Dockerfile $ vi Dockerfile 
Insert the commands as above example into the dockerfile.
-	Run the docker command to build the image
$ docker build –t image_name .
Here ‘-t’ is used to attach a tag (name ) to the image.

	Run the container out of already built docker image


$ docker run –it –p 8100:8100 –v /home/user/user_directory:/workspace --name container_name bash
The above command runs a container out of the image also allows us to get into the shell of container using ‘bash’.
The ‘-p’ tag is to allocate port to the container (8100 in case of Ionic)
The ‘-v’ tag allows to connect the workspace of container to the user directory in host.
Here ‘--name’ is used to assign a name to the container.

	Get into the already running container using the following command
$ docker exec –it container_name bash
	To display all the images in a docker host
$ docker images
	To display all the containers 
$ docker ps –a
	To remove a container $ docker rm –f container_id
	To remove an image $ docker rmi –f image_id
‘-f’ is to remove forcefully.


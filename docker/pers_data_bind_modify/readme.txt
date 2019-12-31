############# To modify existing container ##############
#########################################################


######### Pull ubuntu image
###########
$ docker pull ubuntu:latest



######### Mount container /temp to ~/temp local
###########
$ docker run -it -v ~/temp:/temp ubuntu:latest /bin/bash



######### Do other changes in container and save to new image
###########
[open new terminal]
[Get container_id of existing container which is under modification]
$ docker container ls 
$ docker commit container_id  new_image_name

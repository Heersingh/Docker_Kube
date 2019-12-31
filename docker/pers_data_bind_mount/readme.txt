############# Mount container ##############
############################################


######### Pull ubuntu image
###########
$ docker pull ubuntu:latest



######### Mount container /temp to ~/temp local
###########
$ docker run -it -v ~/temp:/temp ubuntu:latest /bin/bash


######### copy Helloworld application to ~/temp local
###########



######### Run Helloworld inside container shell
###########
$ ./temp/helloworld

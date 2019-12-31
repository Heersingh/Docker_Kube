############# Helloworld container communication on docker network ##############
#################################################################################


######### To build images
###########



####### Pull pre-built images
##########
$ docker pull hssingh/server_cpp:latest
$ docker pull hssingh/client_cpp:latest


####### Communicate containers skiping virtual network (i.e, on host) 
##########
$ docker run -it --net host --name server  hssingh/server_cpp:latest
$ docker run --rm -it --net host --name client  hssingh/client_cpp:latest


####### Publish port
##########
All containers on --network=host can communicate without exposing port (--publish).

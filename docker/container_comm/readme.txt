############# Helloworld container communication on docker network ##############
#################################################################################


######### To build images
###########



####### Pull pre-built images
##########
$ docker pull heersingh/server_cpp:latest
$ docker pull heersingh/client_cpp:latest


####### Run containers same host
##########
$ docker run -it --net host --name server  heersingh/server_cpp:latest
$ docker run --rm -it --net host --name client  heersingh/client_cpp:latest


####### Run containers on different hosts
##########

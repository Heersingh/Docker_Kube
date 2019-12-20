##### Helloword client-server communication 
######This example to show container communication on docker network. 
server_hello application runs a container and client_hello runs in another container;
both applications should be able to communicate on docker network=host type.


####### To pull images and run 
##########
[server]
$ docker pull heersingh/server_hello:latest
$ docker run --rm -it --net=host --name=sample_server  heersingh/server_hello:latest
[client]
$ docker pull heersingh/client_hello:latest
$ docker run --rm -it --net=host --name=sample_client  heersingh/client_hello:latest

######### To build images and run
###########
[server]

[client]



############# Helloworld container communication on docker network ##############
#################################################################################


######### To build images
###########



####### Pull pre-built images
##########
$ docker pull hssingh/server_cpp:latest
$ docker pull hssingh/client_cpp:latest


####### Create new private docker virtual network 'bridge' 
##########
[Create docker network]
$ docker network create --subnet=192.0.0.0/16 --gateway=192.0.0.1  my_net_bridge
[Server]
$ docker run -it --rm  --name server --net my_net_bridge --ip 192.0.0.2  hssingh/server_cpp:latest 
[client]
$ docker run -it --rm  --name client --net my_net_bridge --ip 192.0.0.3  hssingh/client_cpp:latest 



####### Use default private docker virtual network 'bridge' 
##########
[server]
$ docker run -it --rm --name server --network bridge hssingh/server_cpp
[To know server IP]
$ docker network inspect bridge
[client]
$ docker run -it --rm --name client --network bridge hssingh/client_cpp
[To know client IP]
$ docker network inspect bridge



####### NOTE: Publish port
##########
All containers on a same virtual docker network can communicate without exposing port (--publish).

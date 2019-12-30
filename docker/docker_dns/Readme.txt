############################ Docker DNS ##################################
Docker daemon has docker dns which is refered by containers to find other
containers on a custom docker virtual network. Container finds each-other
by contaier name instead of container IP address.
##########################################################################



############### Custome network
#########################
[To create custome network 'bridge']
$ docker network create my_net_name

[Run two any container]
$ docker container run --rm --name nginx_1 --network my_net_name nginx
$ docker container run --rm --name nginx_2 --network my_net_name nginx

[Container by name - usage of docker dns]
$ docker container exec -it nginx_1 ping nginx_2


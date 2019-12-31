############# Persistance Data: Volumes ##############
######################################################


######### mysql image
###########
$ docker pull mysql




######### mysql dockerfile
###########
VOLUME /var/lib/mysql

[Destination mountpoint]
$ docker image inspect mysql




######### Source mountpoint
###########
[Run mysql without -v]

[Host source mountpoint]
$ docker container inspect <mysql-container>

[Run mysql with -v]
$ docker <...> -v my_sql:/var/lib/mysql mysql



######### Check data persistancy
############
[Remove mysql container]

[See volumes]
$ docker volume ls






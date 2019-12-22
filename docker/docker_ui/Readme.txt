############### docker UI portainer ###########
###############


######### Pull portainer image and run
######
$ docker run -d -p 9000:9000 -v /var/run/docker.sock:/var/run/docker.sock   -v portainer_data:/data portainer/portainer


######### Know docker network interface IP - docker0
#######
$ ifconfig

######### In mozila browser 
#######
http://172.17.0.1:9000



######## Create portainer login use
#######
Home should be displayed

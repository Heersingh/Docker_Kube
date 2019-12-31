############## Creating image from scratch ############
##############


##### Compile source code with static flag
###########
$ g++ main.cpp --static


##### Build image
###########
$ docker built -t hello_cpp .


##### Run container
###########
$ docker run --rm -it --name sample_hello hello_cpp


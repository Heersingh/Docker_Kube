FROM alpine

############## shell form #################################
# command runs inside the shell "/bin/sh -c".
# /bin/sh -c" shell runs as parent process with PID1.
# ping as a child  under shell does not get termination SIG
# on ctrl+c.
# prefer to use exec form
###########################################################
#ENTRYPOINT  ls /usr
#ENTRYPOINT ping www.yahoo.com


############################################################
# If use shell format for ENTRYPOINT, CMD is ignored
############################################################
#ENTRYPOINT ls /var
#CMD echo $HOME #this is ignored

#################### exec form #############################
#- exec form does not have shell by default hence should be 
# mentioned explicitly like "/bin/sh", "-c" below.
############################################################
#ENTRYPOINT ["/bin/sh", "-c", "echo", "$HOME"] 
#CMD ["ping", "www.yahoo.com"]


############################################################
# Use entrypoint if docker container run same exe hardcoded
# in dockerfile.
# If multiple CMD in dockerfile then last CMD will be executed
############################################################
#CMD ls /var
#CMD ls /usr



######################## CMD as argument  #################
# If use 'exec' format for entrypoint, CMD arguments are
# appended after.
###########################################################
#ENTRYPOINT ["ls", "/usr"]
#CMD ["/var"]



##################### Override CMD #######################
# Anything after the imagename in the 'docker run' command
# overrides  CMD.
##########################################################
ENTRYPOINT ["ping"]
CMD ["www.yahoo.com"]







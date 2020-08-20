# Install FROM UBUNTU IMAGE
FROM ubuntu:latest

#Author of the Docker File
# MAINTAINER Pictolearn Note: MAINTAINER has been deprecated for LABEL, 
# LABEL is a key value pair 
LABEL "Maintainer"="Pradeep Joshi"

# NOTE and WARNING: ORACLE JDK is no longer licensed.
# use JDk 11 
FROM store/oracle/jdk:11

#use maven
From maven:latest

# ADD a directory called docker-git-hello-world inside the UBUNTU IMAGE where you will be moving all of these files under this 
# DIRECTORY to
ADD . /usr/local/DockerTest

# AFTER YOU HAVE MOVED ALL THE FILES GO AHEAD CD into the directory and run mvn assembly.
# Maven assembly will package the project into a JAR FILE which can be executed
RUN cd /usr/local/DockerTest && mvn clean install

#THE CMD COMMAND tells docker the command to run when the container is started up from the image. In this case we are
# executing the java program as is to print Hello World.
CMD ["java", "-cp", "/usr/local/DockerTest/target/DockerTest-0.0.1-SNAPSHOT-jar-with-dependencies.jar", "com.pj.learn.DockerMVNTest"]

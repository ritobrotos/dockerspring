# dockerspring

This is a basic Spring Boot project which has been created with the purpose of deploying it in docker.

This project doesn't have any dependency added to it.

There is only one endpoint exposed for this service which prints <b>Hello Docker World</b> when you hit the http://localhost:8080/ endpoint.

This project also contains a sample Dockerfile which can be used to create the Docker Image.

Before creating the docker image we need to create the Application Jar which will be deployed. The command for creating the jar is:
<br>$ mvn package

We will be pointing to the same Jar in our Dockerfile.

The command for creating the docker image from the Dockerfile is:  
$ docker build -t springio/gs-spring-boot-docker .
<br>Make sure the command is being run in the directory where the Dockerfile is present.

After the Docker Image is build successfully, next step will be to run the docker image. The command for the same:
<br>$ docker run -p 8080:8080 springio/gs-spring-boot-docker

Now you can view the Application Home Page here: http://localhost:8080/
                                 
To stop the docker image from running just terminate the program by pressing the control(^) + C key.

# Lab-08 ARSW
This programm allow multiple users to draw in a board using realtime
2024/07/09


## Architecture 

![Lab08 (1)](https://github.com/Parralol/Lab08ARSW/assets/110953563/f1ebc18c-764a-4e4b-96c9-63dfad1a7603)

As seen by this diagram we can see the run time in which each user connects via browser to the host using http and the 8080 port, and this browser will be supported by a React mounted client that works with ReactDOM that creates a Root that renders the editor, this editor supports the canvas that each user will be using, this canvas contains a svrStatus object that contains the connection status with the server, a comunicationWS object that works with the React.Ref library and the myp5 object that mantains the canvas.

the BBCanvas uses the WSBBChannel which purpose is to mantain connections and send data to the server, this uses the BBServiceURL to initialize the URL given X host, then communicates to the server via WebSockets and references either /bbService or /status paths, the interactiveblackboardApplication validates each path given and returns the corresponding result with each point given and broadcast all points that are getting sent to the server.

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

### Prerequisites

First you need the following java version (command to see your current java version below)

```
java -version
```

![image](https://github.com/Parralol/Lab05ARSW/assets/110953563/87192abf-bebd-4d74-ad1e-e62a94405c43)

to see the maven version we are using we need to enter the following command, also this is the version of Maven this programm uses

```
mvn -version
```

![image](https://github.com/Parralol/Lab05ARSW/assets/110953563/8711cee6-e4ba-47ae-b46c-8984142890bb)


### Installing

First clone this proyect into your own system, then 

```
mvn clean package
```

### Acceptance test

![image](https://github.com/Parralol/Lab08ARSW/assets/110953563/c6650372-5598-4b8a-8c74-6f20fe3ea086)

This test is run in a deployed service on EC2 as seen in the image

![image](https://github.com/Parralol/Lab08ARSW/assets/110953563/36dfcafb-357f-4d01-bdab-c2838557b13a)

As seen here the program works succesfully on an EC2 instance painting everything the two users ask.



## Generating javadoc

Simply enter the following commands

```
mvn javadoc:javadoc
```

```
mvn javadoc:jar
```

```
mvn javadoc:aggregate
```

```
mvn javadoc:aggregate-jar
```

```
mvn javadoc:test-javadoc 
```

## Deployment

**IN ORDER FOR THIS PROGRAM TO WORK, YOU'LL NEED TO EXECUTE THE PROGRAM ON THE FOLDER YOU WANT TO WORK WITH, WITH THE FILES YOU WANT TO WORK WITH**

if you want to use the programm after using the package command we use

```
mvn spring-boot:run
```

after the server has initialized, you'll have to type in the browser

http://localhost:8080


## Built With

* [Maven](https://maven.apache.org/) - Dependency Management
* [Java](https://www.oracle.com/java/technologies/) - Programming Language
* [HTML 5](https://html.spec.whatwg.org/multipage/) - HiperText Markup Lenguaje
* [Spring](https://spring.io/) - Framework
* [React](https://es.react.dev/)- Front-end Libray
## Versioning

We use [SemVer](http://semver.org/) for versioning. For the versions available, see the [tags on this repository](https://github.com/your/project/tags). 

## Authors

* **Santiago Parra** - *Initial work* - [Parralol](https://github.com/Parralol)

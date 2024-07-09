# Lab-08 ARSW
This programm allow multiple users to draw in a board using realtime
2024/07/09


## Architecture 

![Lab05 (1)](https://github.com/Parralol/Lab05ARSW/assets/110953563/6b9a1c06-4762-4ab5-bc01-09e6b77a9310)

As seen by the following diagram the user connects via browser to use the program, then he must connect via http using the 8080 port (tomcat), the program is deployed in a EC2 instance which runs the program with the Spring framework, this program is running two java classes, the main one being Lab05Application and the controller being Lab05Controller, the way the main class comunicates with the controller is via paths, the main path being _/calculator_ is the first one to be run, then the responses the controller gives are being delivered as infomation in the post type paths _/case_ & _/calculate_

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

# Service Oriented Architecture

## Overview
In this homework, you will split the Quote monolith into multiple services that
run independently.  You should need three services - an API gateway, a quote
service and an author service.

Your architecture should look something like the following -

![Apps Architecture](./architecture.png)

If wish to create a new Spring project for the services, the Spring initializer is a quick way of create the necessary project structure -

http://start.spring.io/


## API Gateway

The API gateway is a common solution to hide the server side complexities from
the client.  It is similar to the
[facade pattern](https://en.wikipedia.org/wiki/Facade_pattern) in object
oriented design.

The API gateway will receive requests from the browsers and then call the necessary services to handle the request.  The API should implement the URLs currently used in the client code.

## Quote and Author Service
The quote and author services should implement a REST API to handle the business logic for its domain model.

## Considerations
You will need to make some decisions when breaking up the monolith.  You should use the [12-factor app](https://12factor.net/) methodology to guide your decisions.

To get full credit, your application should follow these factors -
* Code base
* Config

## Sources
* [Building REST Service in Spring](https://spring.io/guides/gs/rest-service/)
* [Springs RestTemplate](http://www.baeldung.com/rest-template)

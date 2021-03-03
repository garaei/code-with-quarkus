# code-with-quarkus project

This project uses Quarkus, the Supersonic Subatomic Java Framework.

If you want to learn more about Quarkus, please visit its website: https://quarkus.io/ .

## Running the application in dev mode

You can run your application in dev mode that enables live coding using:
```shell script
./mvnw compile quarkus:dev
```

> **_NOTE:_**  Quarkus now ships with a Dev UI, which is available in dev mode only at http://localhost:8080/q/dev/.

## Packaging and running the application

The application can be packaged using:
```shell script
./mvnw package
```
It produces the `quarkus-run.jar` file in the `target/quarkus-app/` directory.
Be aware that it’s not an _über-jar_ as the dependencies are copied into the `target/quarkus-app/lib/` directory.

If you want to build an _über-jar_, execute the following command:
```shell script
./mvnw package -Dquarkus.package.type=uber-jar
```

The application is now runnable using `java -jar target/quarkus-app/quarkus-run.jar`.

## Creating a native executable

You can create a native executable using: 
```shell script
./mvnw package -Pnative
```

Or, if you don't have GraalVM installed, you can run the native executable build in a container using: 
```shell script
./mvnw package -Pnative -Dquarkus.native.container-build=true
```

You can then execute your native executable with: `./target/code-with-quarkus-1.0.0-SNAPSHOT-runner`

If you want to learn more about building native executables, please consult https://quarkus.io/guides/maven-tooling.html.

## Related guides

- OpenID Connect Client ([guide](https://quarkus.io/guides/security-openid-connect-client)): Use OpenID Connect Client to get and refresh access tokens
- Quarkus Extension for Spring Security API ([guide](https://quarkus.io/guides/spring-security)): Secure your application with Spring Security annotations
- Quarkus Extension for Spring Scheduled  ([guide](https://quarkus.io/guides/spring-scheduled)): Schedule tasks with Spring Scheduling
- RESTEasy JAX-RS ([guide](https://quarkus.io/guides/rest-json)): REST endpoint framework implementing JAX-RS and more
- Quarkus Extension for Spring Web API ([guide](https://quarkus.io/guides/spring-web)): Use Spring Web annotations to create your REST services
- Quarkus Extension for Spring Data JPA API ([guide](https://quarkus.io/guides/spring-data-jpa)): Use Spring Data JPA annotations to create your data access layer
- Quarkus Extension for Spring Boot properties ([guide](https://quarkus.io/guides/spring-boot-properties)): Use Spring Boot properties annotations to configure your application
- MongoDB client ([guide](https://quarkus.io/guides/mongodb)): Connect to MongoDB in either imperative or reactive style
- Quarkus Extension for Spring Cache API ([guide](https://quarkus.io/guides/spring-cache)): Use Spring Cache annotations
- OpenID Connect ([guide](https://quarkus.io/guides/security-openid-connect)): Secure your applications with OpenID Connect Adapter and IDP such as Keycloak
- Camel Google Calendar ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/google-calendar.html)): Perform various operations on a Google Calendar
- Quarkus Extension for Spring Data REST ([guide](https://quarkus.io/guides/spring-data-rest)): Generate JAX-RS resources for a Spring Data application
- Quarkus Extension for Spring DI API ([guide](https://quarkus.io/guides/spring-di)): Define your dependency injection with Spring DI
- Security JPA ([guide](https://quarkus.io/guides/security-jpa)): Secure your applications with username/password stored in a database via JPA

## Provided examples

### RESTEasy JAX-RS example

REST is easy peasy with this Hello World RESTEasy resource.

[Related guide section...](https://quarkus.io/guides/getting-started#the-jax-rs-resources)

### RESTEasy JSON serialisation using Jackson

This example demonstrate RESTEasy JSON serialisation by letting you list, add and remove quark types from a list. Quarked!

[Related guide section...](https://quarkus.io/guides/rest-json#creating-your-first-json-rest-service)

### Spring Web example

Spring, the Quarkus way! A Hello World Spring Web Controller.

[Related guide section...](https://quarkus.io/guides/spring-web#greetingcontroller)

Very simple "`Hello, World`" RESTful web service created by Spring, followed with this guide: [Building a RESTful Web Service](https://github.com/spring-guides/gs-rest-service?tab=readme-ov-file).

== What I Built according to the guide

A service that will accept HTTP GET requests at
`http://localhost:8080/greeting`.

It will respond with a JSON representation of a greeting, as the following listing shows:

====
[source,json]
----
{"id":1,"content":"Hello, World!"}
----
====

Can customize the greeting with an optional `name` parameter in the query string, as
the following listing shows:

====
[source,text]
----
http://localhost:8080/greeting?name=User
----
====

The `name` parameter value overrides the default value of `World` and is reflected in the
response, as the following listing shows:

====
[source,json]
----
{"id":1,"content":"Hello, User!"}
----
====

== How to Run
In the project directory, run the following command:
```shell
./mvnw clean install  # maybe not necessary
./mvnw spring-boot:run
```
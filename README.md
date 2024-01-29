# camel-workshop

Introduction to Apache Camel & Quarkus software development

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

The application is now runnable using `java -jar target/quarkus-app/quarkus-run.jar`.

If you want to build an _über-jar_, execute the following command:

```shell script
./mvnw package -Dquarkus.package.type=uber-jar
```

The application, packaged as an _über-jar_, is now runnable using `java -jar target/*-runner.jar`.

## Creating a native executable

You can create a native executable using:

```shell script
./mvnw package -Dnative
```

Or, if you don't have GraalVM installed, you can run the native executable build in a container using:

```shell script
./mvnw package -Dnative -Dquarkus.native.container-build=true
```

You can then execute your native executable with: `./target/camel-workshop-1.0-SNAPSHOT-runner`

If you want to learn more about building native executables, please consult https://quarkus.io/guides/maven-tooling.

## Related Guides

- Camel Platform HTTP ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/platform-http.html)):
  Expose HTTP endpoints using the HTTP server available in the current platform
- Camel Core ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/core.html)): Camel core
  functionality and basic Camel languages: Constant, ExchangeProperty, Header, Ref, Simple and Tokenize
- Camel SEDA ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/seda.html)): Asynchronously
  call another endpoint from any Camel Context in the same JVM
- Camel JacksonXML ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/jacksonxml.html)):
  Unmarshal an XML payloads to POJOs and back using XMLMapper extension of Jackson
- Camel Data Format ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/dataformat.html)): Use a
  Camel Data Format as a regular Camel Component
- Camel Jackson ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/jackson.html)): Marshal
  POJOs to JSON and back using Jackson
- Camel HTTP ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/http.html)): Send requests to
  external HTTP servers using Apache HTTP Client 5.x
- Camel Rest ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/rest.html)): Expose REST
  services and their OpenAPI Specification or call external REST services
- Camel Qute ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/qute.html)): Transform messages
  using Quarkus Qute templating engine

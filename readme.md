source : https://github.com/spring-guides/gs-actuator-service

### How to run 

```shell
$ mvn clean compile
$ java -jar target/gs-actuator-service-0.1.0-SNAPSHOT.jar
$ curl localhost:8080/hello-world
curl: (52) Empty reply from server
```

### ---

f you use Maven, you can run the application by using `./mvnw spring-boot:run`. Alternatively, you can build the JAR file with `./mvnw clean package` and then run the JAR file, as follows:

```shell
java -jar target/gs-actuator-service-0.1.0-SNAPSHOT.jar
```



You can test that it is working on port 9000 by running the following commands in a terminal:

```shell
$ curl localhost:8080/hello-world
curl: (52) Empty reply from server
$ curl localhost:9000/hello-world
{"id":1,"content":"Hello, Stranger!"}
$ curl localhost:9001/actuator/health
{"status":"UP"}
```
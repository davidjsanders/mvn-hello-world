# maven-hello-world
Simple hello world Dockerized. 

To build:
```
cd maven

docker build -t <tagit> .
```

To run with JDK 11.0.1:

```
cd maven

docker run --rm -it -e JAVA_HOME=/usr/lib/jvm/jdk-11.0.1 -v $(pwd)/my-app:/my-app mavenimg -c "cd /my-app/; mvn package; \$JAVA_HOME/bin/java -cp target/my-app-1.0-SNAPSHOT.jar com.mycompany.app.App"
```

To run with JDK 1.8.181:

```
cd maven

docker run --rm -it -e JAVA_HOME=/usr/lib/jvm/java-1.8.0-openjdk-amd64 -v $(pwd)/my-app:/my-app mavenimg -c "cd /my-app/; mvn package; \$JAVA_HOME/bin/java -cp target/my-app-1.0-SNAPSHOT.jar com.mycompany.app.App"
```
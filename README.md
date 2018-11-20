# maven-hello-world
Simple hello world Dockerized. 

To build:
```
cd maven

docker build -t <tagit> .
```

To run:

```
cd maven

docker run --rm -it -v $(pwd)/my-app:/my-app mavenimg -c "cd /my-app/; mvn package; java -cp target/my-app-1.0-SNAPSHOT.jar com.mycompany.app.App"
```

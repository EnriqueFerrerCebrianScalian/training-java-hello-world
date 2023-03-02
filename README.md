# CI / CD Strategy with Docker

## Create Java APP Docker image
```bash
$ docker build -t scalian_training-java-hello-world-build:0.0.1 -f devops/build.Dockerfile --network host .
$ docker run -d --rm -p 8085:8080  --name java-app   scalian_training-java-hello-world:0.0.1
$ curl localhost:8084/hello
$ docker stop java-app
$ cd ..

$ docker run --rm -w . -v ${PWD}/src:/app/src -v ./pom.xml:/app/pom.xml maven:3.8.6-openjdk-11-slim ls


```

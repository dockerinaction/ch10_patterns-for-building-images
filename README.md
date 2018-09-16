
Build the application with a docker container using the Maven image:

```
docker container run --rm -it -v $(pwd):/project --workdir /project maven:3.5-jdk-10 mvn -f pom.xml clean verify
```

Build the application runtime image with:

```
docker image build -t ch11_separate-build-and-runtime --file runtime.df .
```

Run the application with:

```
docker container run --rm -it ch11_separate-build-and-runtime
```


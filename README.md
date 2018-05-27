# Experiment | Apache Mitigating DOS

## Usage

Original Apache

```
$ docker build --tag my-apache-normal --file ./Dockerfile-Original .
$ docker run --name my-apache-normal --publish 8080:80 my-apache-normal
```

with [mod\_dosdetector](https://github.com/stanaka/mod_dosdetector)

```
$ docker build --tag my-apache-mitigating-dos --file ./Dockerfile-DosDetecting .
$ docker run --name my-apache-mitigating-dos --publish 8081:80 my-apache-mitigating-dos
```

Access http://localhost:8080/ and http://localhost:8081/

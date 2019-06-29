# docker-geoserver
[![Build Status](https://travis-ci.org/sogis/docker-geoserver.svg?branch=master)](https://travis-ci.org/sogis/docker-geoserver)
 
Building:
```
docker build -t sogis/geoserver:2.15.1 .
```

The image is built automatically by Travis CI and is available from https://hub.docker.com/r/sogis/geoserver.

Running with the built in data directory:
```
docker run --rm --name sogis-geoserver -d -p 8080:8080 sogis/geoserver:2.15.1
```

Running with a specific data directory:
```
docker run --rm --name sogis-geoserver -d -p 8080:8080 -v /path/to/local/data_dir:/var/local/geoserver sogis/geoserver:2.15.1
```

Mount another directory with e.g. geodata:
```
docker run --rm --name sogis-geoserver -d -p 8080:8080 -v /Users/stefan/tmp/geodata:/geodata -v /Users/stefan/tmp/data_dir:/var/local/geoserver sogis/geoserver:2.15.1
```

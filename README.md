# docker-geoserver

Building:
```
docker build -t sogis/geoserver:2.15.1 .
```

Running with the built in data directory:
```
docker run --rm --name sogis-geoserver -d -p 8080:8080 sogis/geoserver:2.15.1
```

Running with a specific data directory:
```
docker run --rm --name sogis-geoserver -d -p 8080:8080 -v /path/to/local/data_dir:/var/local/geoserver sogis/geoserver:2.15.1

docker run --rm --name sogis-geoserver -d -p 8080:8080 -v /Users/stefan/tmp/geodata:/geodata -v /Users/stefan/tmp/data_dir:/var/local/geoserver sogis/geoserver:2.15.1
```
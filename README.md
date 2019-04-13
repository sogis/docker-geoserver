# docker-geoserver

```
docker build -t sogis/geoserver .

docker run --rm -d -p 8080:8080 -v /Users/stefan/tmp/geoserver-data_dir:/var/local/geoserver -v /Volumes/Samsung_T5/singletiff:/data --name=MyGeoServerInstance sogis/geoserver

```


# dockerfile-gcloud-cli
Dockerfile with gcloud cli and ansible to upload a gke cluster.

### Build image
```
cd ./dockerfile/
```
```
docker build -t gcloud-cli:0.0.1 -f Dockerfile.gcloud-cli .
```


**if you want to reduce image size then install docker-slim**
```
curl -L -o ds.tar.gz https://downloads.dockerslim.com/releases/1.39.1/dist_linux.tar.gz
```
```
tar -xvf ds.tar.gz
mv  dist_linux/docker-slim /usr/local/bin/
mv  dist_linux/docker-slim-sensor /usr/local/bin/
docker-slim update
```
```
docker-slim build --target gcloud-cli:0.0.1 --http-probe=false
```

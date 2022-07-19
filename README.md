# GDAL with Oracle
It can be a hussle to get this to work.
Sharing is caring, so here you got my result.

# How to use
Build the Docker image and run it.
It should work as it is.

1. Run `docker build -t gdal-oci .`
2. Run `docker run -it gdal-oci`
3. Run in container `ogr2ogr --formats | grep OCI`

This should result in: `OCI -vector- (rw+): Oracle Spatial`

# How I did it
These are the steps I took to build GDAl with OCI driver:

1. I took the ubuntu small Docker file from the [GDAL github repo](https://github.com/OSGeo/gdal/blob/master/docker/ubuntu-small/Dockerfile);
2. I added the installation steps to install OCI to the Dockerfile based on [fegyi001's repo](https://github.com/fegyi001/docker-gdal-oci);


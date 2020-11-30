# SMT Horizon

This is the Smart48 official Laravel Horizon image based on the Laradock Horizon image running on PHP 7.4. The image is used together with the Laravel, Nginx, Workspace and Worker image to run the Laravel PHP application with ease.
## Docker Build

To build for our own Smart48 Docker Hub repository we use

`docker build . -t smart48/smt-horizon`

This will build with the tag using our organization's name and name for the image. Make sure Docker is running or see something like Cannot connect to the Docker daemon at unix:///var/run/docker.sock. Is the docker daemon running?

## Test

You can test the build image using:

`docker run --name smt-horizon -d smart48/smt-horizon:latest`

To see if it is there we do a 

```
smt-horizon git:(main) ✗ docker ps |grep smt
4e6570c66954        smart48/smt-horizon:latest            "/usr/bin/supervisor…"   3 minutes ago       Up 3 minutes      smt-horizon
```

## Docker Push

To push the built image you run:

`docker image push smart48/smt-horizon`
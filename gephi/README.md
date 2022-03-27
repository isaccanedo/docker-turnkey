# Gephi

[![Version](https://img.shields.io/badge/Version-0.9.2-success)](#)
[![GitHub](https://img.shields.io/badge/Github-turnkey-success)](https://github.com/atb00ker/docker-turnkey/tree/master/gephi)
[![Dockerhub](https://img.shields.io/badge/docker--hub-turnkey-blue)](https://hub.docker.com/repository/docker/atb00ker/docker-turnkey)
[![Pull](https://img.shields.io/badge/Pull-atb00ker/docker--turnkey:gephi-blue)](#)

Gephi: https://gephi.org/

### Usage

1. Allow connection to the X server: `xhost local:root`

2. Run the container:

```bash
docker run --rm --name gephi \
           --volume /tmp/.X11-unix:/tmp/.X11-unix \
           --volume $HOME/graph/:/root/ \
           --env DISPLAY=$DISPLAY \
           atb00ker/docker-turnkey:gephi
```

3. If you save the files using gephi, they are created by `root` user, hence `sudo chmod 777 $HOME/graph/*` can be used to give the access of the file to your user.

### Build

```bash
docker build --file $PWD/gephi/Dockerfile $PWD/gephi \
             --tag atb00ker/docker-turnkey:gephi
```

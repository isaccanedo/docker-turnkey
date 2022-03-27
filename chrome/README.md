# Chrome

[![Version](https://img.shields.io/badge/Version-80.0-success)](#)
[![GitHub](https://img.shields.io/badge/Github-turnkey-success)](https://github.com/atb00ker/docker-turnkey/tree/master/chrome)
[![Dockerhub](https://img.shields.io/badge/docker--hub-turnkey-blue)](https://hub.docker.com/repository/docker/atb00ker/docker-turnkey)
[![Pull](https://img.shields.io/badge/Pull-atb00ker/docker--turnkey:chrome-blue)](#)

Chrome: https://www.google.com/chrome/

### Usage

1. Allow connection to the X server: `xhost local:root`

2. Run the container:

```bash
docker run --rm --name chrome \
           --net host \
           --env DISPLAY=unix$DISPLAY \
           --volume /tmp/.X11-unix:/tmp/.X11-unix \
           --volume /dev/shm:/dev/shm \
           --device /dev/dri:/dev/dri \
           atb00ker/docker-turnkey:chrome
```

### Build

```bash
docker build --file $PWD/chrome/Dockerfile $PWD/chrome \
             --tag atb00ker/docker-turnkey:chrome
```

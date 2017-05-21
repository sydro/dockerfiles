# Docker Atom Editor Beta Version

Docker image for [Atom Editor (beta version)](https://atom.io/).

This repository contains build of Atom beta version for developing.

## Starting a Atom container

```
docker run -d \
   --cpuset-cpus 0 \
   -v /etc/localtime:/etc/localtime:ro \
   -v /tmp/.X11-unix:/tmp/.X11-unix \
   -v $HOME/.Xauthority:/home/atom/.Xauthority \
   -v $HOME/.atom:/home/atom/.atom \
   -e DISPLAY=unix$DISPLAY \
   -e GDK_SCALE \
   -e GDK_DPI_SCALE \
   --device /dev/dri \
   --name atom-beta \
   sydro/atom-beta
```

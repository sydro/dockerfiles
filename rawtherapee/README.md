# Docker Rawtherapee

Docker image for [Rawtherapee](http://rawtherapee.com/).

## Starting a Rawtherapee container

```
docker run -d \
   --cpuset-cpus 0 \
   -v /etc/localtime:/etc/localtime:ro \
   -v /tmp/.X11-unix:/tmp/.X11-unix \
   -v $HOME/Images:/home/rawtherapee/Immagini \
   -v $HOME/.config:/home/rawtherapee/.config \
   -e DISPLAY=unix$DISPLAY \
   -e GDK_SCALE \
   -e GDK_DPI_SCALE \
   --device /dev/dri \
   --name rawtherapee \
   sydro/rawtherapee

```

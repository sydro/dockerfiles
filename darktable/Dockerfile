FROM ubuntu:16.04

RUN apt-get update && \
    apt-get -y install debhelper dpkg-dev fakeroot wget && \
    apt-get -y build-dep darktable && \
    cd /root && wget https://github.com/darktable-org/darktable/releases/download/release-2.4.0/darktable-2.4.0.tar.xz && \
    tar -xvf darktable-2.4.0.tar.xz && \
    cd darktable-2.4.0 && \
    ./build.sh --prefix /opt/darktable --build-type Release && \
    cmake --build "/root/darktable-2.4.0/build" --target install -- -j4

RUN useradd -ms /bin/bash darktable

USER darktable
WORKDIR /home/darktable

CMD /opt/darktable/bin/darktable

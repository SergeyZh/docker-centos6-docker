# docker-centos6-docker
Docker in docker

Usage
=====

Run image for Docker:
```
docker run -it --rm --privileged -v /dev:/dev -v /lib/modules:/lib/modules sergeyzh/centos6-docker
```

Run Docker inside image above:
```
bash-4.1# docker -d &
[1] 193
bash-4.1# INFO[0000] +job serveapi(unix:///var/run/docker.sock)
INFO[0000] Listening for HTTP on unix (/var/run/docker.sock)
WARN[0000] Udev sync is not supported. This will lead to unexpected behavior, data loss and errors
INFO[0000] +job init_networkdriver()
INFO[0000] -job init_networkdriver() = OK (0)
WARN[0000] mountpoint for memory not found
INFO[0000] Loading containers: start.

INFO[0000] Loading containers: done.
INFO[0000] docker daemon: 1.6.2 7c8fca2/1.6.2; execdriver: native-0.2; graphdriver: devicemapper
INFO[0000] +job acceptconnections()
INFO[0000] -job acceptconnections() = OK (0)
INFO[0000] Daemon has completed initialization

bash-4.1#
bash-4.1#
bash-4.1# docker ps
INFO[0004] GET /v1.18/containers/json
INFO[0004] +job containers()
INFO[0004] -job containers() = OK (0)
CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS              PORTS               NAMES
bash-4.1#

```


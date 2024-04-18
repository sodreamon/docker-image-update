# docker-image-update

It is intended to change only the container image, leaving the existing settings of the Docker container's network, ip, port, env, restart, name, etc. intact.

## Usage
```
./docker-image-update -f -d -ti --add-host {host} {existing container name} {new image}

-f : remove existing container force
-d : detach
-ti : interactive
--add-host : same as docker --add-host param

ex) docker-image-update -f -d -ti --add-host testdomain.test:10.50.0.2 testcontainer newimage:newtag
```

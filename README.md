# docker-image-update

It is intended to change only the container image, leaving the existing settings of the Docker container's network, ip, port, env, restart, name, etc. intact.

## Install
```
git clone https://github.com/sodreamon/docker-image-update.git
sudo cp docker-image-update/docker-image-update /usr/local/bin/docker-image-update
chmod 755 /usr/local/bin/docker-image-update
```

## Usage
```
docker-image-update -f -d -ti --add-host {host} {existing container name} {new image}

-f : remove existing container force
-d : detach
-ti : interactive
--add-host : same as docker --add-host param

ex) docker-image-update -f -d -ti --add-host testdomain.test:10.50.0.2 testcontainer newimage:newtag
```

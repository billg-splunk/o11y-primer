# Docker

This section will cover as much about docker to be dangerous. There are a bunch of great resources for Docker. This is meant to be a cheat sheet on common ways to use Docker, in particular in setting up O11y examples.

## Installation Notes
Follow the [instructions here](https://docs.docker.com/engine/install/). And follow the [post-installation notes here](https://docs.docker.com/engine/install/linux-postinstall/) that ensure your user can run docker without needing to use ```sudo```.

Follow the [instructions here](https://docs.docker.com/compose/install/) to install Docker Compose. Docker Compose makes it easy to run multi-container Docker applications.

## Testing out your docker install

## Creating your own Docker repo

Starting your own repo:
```
docker run -d -p 5000:5000 --name registry registry:2.7
```

And verifying it:
```
docker logs -f registry
```

Then you can push to it, like:
```
docker push localhost:5000/ubuntu
```
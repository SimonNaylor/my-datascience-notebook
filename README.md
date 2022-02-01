# my-datascience-notebook
Small project getting a docker python data science development environment up and running.

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/SimonNaylor/my-datascience-notebook/main)

The built image is [hosted on Docker-Hub](https://hub.docker.com/repository/docker/naylorsimj/my-datascience-notebook).

## Using this repo
### With `docker`
Build:

```bash
docker build fill-in-the-rest
This below is what is requred to build the docker image.
```

Run:

```bash
docker run fill-in-the-rest
docker run --rm -p 10000:8888 -v "${PWD}":/home/jovyan/work jupyter/datascience-notebook:b418b67c225b
```

### With `docker-compose`
Build and run:

```bash
docker-compose up
version: "3.9"  # optional since v1.27.0
services:
  jupyter:
    image: jupyter/datascience-notebook:b418b67c225b
    ports:
      - "8888:8888"
    volumes:
      - .:/home/jovyan/work
```

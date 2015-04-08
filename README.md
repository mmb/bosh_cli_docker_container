Build a Docker container with the latest version of the BOSH CLI.

This repo is connected to a Docker Hub automated build. Whenever it is
pushed to the container on Docker Hub will be updated.

Usage:

```
docker pull mm62/bosh_cli
docker run -it --rm mm62/bosh_cli
docker run -it --rm mm62/bosh_cli version
```

To persist your BOSH config outside the container:

```
touch ~/.bosh_config

docker run -it --rm -v ~/.bosh_config:/bosh_config -e BOSH_CONFIG=/bosh_config 36a3672976ef target
```

To bump this repo to latest version of the BOSH CLI on rubygems.org:

`./bump`

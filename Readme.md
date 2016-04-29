# Cloud9 v3 Dockerfile

This repository contains Dockerfile of Cloud9 IDE for Docker's automated build published to the public Docker Hub Registry.

## Base docker image

- [hub.docker.com](https://registry.hub.docker.com/u/eeacms/cloud9)


## Installation

1. Install [Docker](https://www.docker.com/).

## Usage

    docker run -it -d -p 8080:8080 eeacms/cloud9
    
You can add a workspace as a volume directory with the argument *-v /your-path/workspace/:/workspace/* like this :

    docker run -it -d -p 8080:8080 -v /your-path/workspace/:/workspace/ eeacms/cloud9
    
## Build and run with custom config directory

Get the latest version from github

    git clone https://github.com/eea/eea.docker.cloud9
    cd cloud9-docker/

Build it

    docker build --force-rm=true -t "$USER/cloud9:latest" .
    
And run

    docker run -d -p 8080:8080 -v /your-path/workspace/:/workspace/ $USER/cloud9:latest
   
Enjoy !!    

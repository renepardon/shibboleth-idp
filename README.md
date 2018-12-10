# Build/Run

First, pull this respository. Then execute the following commands:

    docker pull centos:centos7
    docker build --tag="local/shibboleth-idp:latest" .
    docker-compose up -d

Container should be reachable through `https://<docker_host_ip>:4443/idp/`.

# Password

The password used for the certificates is:

> changeme 

# Create a new shibboleth IdP configuration

docker run -it -v $(pwd):/ext-mount unicon/shibboleth-idp init-idp.sh


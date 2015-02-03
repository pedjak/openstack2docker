Purpose
=======

Docker container for converting an [OpenStack|http://www.openstack.org] image 
into the equivalent [Docker|http://www.docker.com] image

Usage
=====

    docker run -e OS_USERNAME=<openstack username> \	
            -e OS_TENANT_NAME=<openstack tenant name> \	
            -e OS_PASSWORD=<openstack password> \
            -e OS_AUTH_URL=<openstack url> \
            -e DOCKER_HOST=<docker host> \
            --privileged \
            --rm \
            -v /dev:/dev \
            pedjak/openstack2docker <openstack image> <docker image tag>

Limitations
===========

OpenStack images may contain only one non-swap partition.
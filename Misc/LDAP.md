---
title: Ldap JF
description: 
published: true
date: 2020-06-17T18:59:52.779Z
tags: 
editor: markdown
---

## Setting Up LDAP
First, you should have Docker installed on your Ubuntu. https://docs.docker.com/install/linux/docker-ce/ubuntu/ , is the official link for installing Docker. Don’t forget to follow post-installation steps in the end.

Then simply run the following command from terminal.
> Replace <kbd>LDAP_ORGANISATION</kbd>, <kbd>LDAP_DOMAIN</kbd>,<kbd>LDAP_ADMIN_PASSWORD</kbd> and <kbd>LDAP_BASE_DN</kbd> with their respective values
{.is-info}


`docker run -p 389:389 --name ldap-service --hostname ldap-service --env LDAP_ORGANISATION="pirate" --env LDAP_DOMAIN="pirate.com" --env LDAP_ADMIN_PASSWORD="admin" --env LDAP_BASE_DN="dc="pirate,dc=com" --volume /data/slapd/database:/var/lib/ldap --volume /data/slapd/config:/etc/ldap/slapd.d --detach osixia/openldap:latest`

It will fetch the image and start the docker container. Port is exposed for accessing the container from another machine and volumes are mapped so your data remains in persistent state.

> (This is not required but makes it a lot easier) 
{.is-warning}

There is a Docker image which provides GUI for its OpenLDAP image, very useful for populating users and groups into OpenLDAP visually. 

docker run --name phpldapadmin-service --hostname phpldapadmin-service --link ldap-service:ldap-host --env PHPLDAPADMIN_LDAP_HOSTS=ldap-service --detach osixia/phpldapadmin:latest
This command will fetch the image and run the container, which will be linked to the previously running container through the link flag.

---
title: OctoPrint
description: 
published: true
date: 2020-04-29T17:43:08.245Z
tags: 
---

# OctoFarm Install and Setup
###### Resources
Test Server http://test.octofarm.net/
Username:demo
Password:demo123
[Website](https://octofarm.net/)
[Github](https://github.com/NotExpectedYet/OctoFarm)

###### Installing docker compose
1. The first step is intalling docker compose. Run this command to download the current stable release of Docker Compose. (Check the latest version [here](https://github.com/docker/compose/releases) and replace 1.25.5 with the newest version)
`sudo curl -L "https://github.com/docker/compose/releases/download/1.25.5/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose`

2. Apply executable permissions to the binary.
`sudo chmod +x /usr/local/bin/docker-compose`

![1.jpg](/octoprint/1.jpg)

3. To test the version number.
`docker-compose --version`

###### Installing OctoFarm
1. Now you need to make the directory where the compose file is going to be.
`sudo mkdir /home/<user>/compose/octofarm`

2. Cd into the directory.
`cd /home/<user>/compose/octofarm`

3. Create your docker compose compose file
`sudo nano docker-compose.yml`

4. Add this to the docker compose (You can change the variables as needed)
```
version: "3.8"
services:
  mongo:
    image: mongo
    restart: always
    volumes:
      - /var/lib/OctoFarm/MongoDB:/data/db

  octofarm:
    container_name: octofarm
    image: octofarm/octofarm
    restart: always
    ports:
      - 4000:4000
    environment:
      - MONGO=mongodb://mongo/octofarm
      - TZ=GMT-7
    volumes:
      - /var/lib/OctoFarm/config:/app/serverConfig
      - /var/lib/OctoFarm/OctoFarm/logs:/app/logs
```
5. Save and exit the docker-compose.yml

6. Run the command `sudo docker-compose up` this will pull the images start Octofarm and create a mongo database
 
7. You should then be able to navigate to http://serverip:4000 then follow the steps to create a new user
> Make sure you enable Cross Origin Resource Sharing (CORS) under the API setting in octoprint
{.is-warning}

![2.jpg](/octoprint/2.jpg)
      
![3.jpg](/octoprint/3.jpg)
     
![4.jpg](/octoprint/4.jpg)

![inked5_li.jpg](/octoprint/inked5_li.jpg) 

![6.jpg](/octoprint/6.jpg)
      
![7.jpg](/octoprint/7.jpg)
 


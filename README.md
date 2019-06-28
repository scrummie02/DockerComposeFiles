# DockerComposeFiles
List of Docker Compose files I use to deploy docker services and stacks
Here is a description of the services


## Nextcloud
This compose file uses the following
* The awesome WonderFall Nextcloud repo found [here](https://hub.docker.com/r/wonderfall/nextcloud/)
* The Alpine version of [Redis](https://hub.docker.com/_/redis/)
* The latest version of [MySQL](https://hub.docker.com/_/mysql)
* ClamAV conatiner to scan uploads found [here](https://github.com/tiredofit/docker-clamav)
* In-line document editing via OnlyOffice [Docker](https://github.com/ONLYOFFICE/Docker-DocumentServer)

Ensure you have enough resources, 4GB is fine if you want torun OnlyOffice.  If you don't want to just remove it.
To take advantage of OnlyOffice and ClamAV you'll need to install the apps in NextCloud and point them to the containers.  


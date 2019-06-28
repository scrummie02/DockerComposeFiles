# Docker Compose Files
List of Docker Compose files I use to deploy docker services and stacks in my Docker Swarm
Here is a description of the services


## Nextcloud
This is a fully functioning NextCloud install with in-line document editing, anti-virus scanning for uploads and using the secure Wonderfall NextCloud image that doesn't run any root user processes and use Alpine Linux to keep things small and secure.  
This compose file uses the following
* The awesome WonderFall Nextcloud repo found [here](https://hub.docker.com/r/wonderfall/nextcloud/)
* The Alpine version of [Redis](https://hub.docker.com/_/redis/)
* The latest version of [MySQL](https://hub.docker.com/_/mysql)
* ClamAV conatiner to scan uploads found [here](https://github.com/tiredofit/docker-clamav)
* In-line document editing via OnlyOffice [Docker](https://github.com/ONLYOFFICE/Docker-DocumentServer)
* Bundled with nginx and PHP 7.x (wonderfall/nginx-php image).
* Automatic installation using environment variables.
* Data and apps persistence.
* Maintenance free anti-virus updates and scanning.
* Easy to read log files for anti-virus reports/auditing


Ensure you have enough resources, 4GB is fine if you want torun OnlyOffice.  If you don't want to just remove it.
To take advantage of OnlyOffice and ClamAV you'll need to install the apps in NextCloud and point them to the containers.  

## PostFix MTA   
[This](https://github.com/scrummie02/DockerComposeFiles/blob/master/postfix_mta.yml) simple to configure Postfix MTA you can use to connect to your Gmail account.  This is great for a simple MTA that you can use to email yourself alerts of other things.  This isn't to be used exteranlly!  It is used for your local apps to use to send you messages, alerts or even documents.  

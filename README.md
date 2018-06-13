# Docker ELK stack modified to support net2Host

Addtional docker containers compared to docker-elk:
 - redis - Used to store correlation information
 - correlate - Used to correlate logs
 - nxlog - accepts windows firewall logs
 - brologread - fetches bro logs.

You will need to alter docker-compose.yml to fit your system:
 - Set JVM size for Elastic
 - Change bro current mount for brologread

Docker compose config base on:
https://github.com/deviantony/docker-elk

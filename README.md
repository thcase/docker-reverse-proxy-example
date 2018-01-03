# Introduction
The purpose of this project is to document basic load balancing and reverse proxy using Docker and NGINX.

# Prerequisites
This project depends on Docker 17.03 or greater and Docker-Compose.

# Details
This project uses Docker Compose to create three NGINX instances.

* Web 1 (web1) - First Web Instance where  Docker Compose includes the html folder as an attached volume
* Web 2 (web2) - Second Web Instance where Docker Compose includes the html folder as an attached volume
* Load Balancer (lb) - Load balancer that serves requests between the two instances, also has virtual directories mapped for /web1 and /web2 that direct to the specific web instance.

# Build
To build this file, at the project root, issue the following command:

```commandline
docker-compose up -d
```

To remove the running instances, issue the following command:

```commandline
docker-compose down
```
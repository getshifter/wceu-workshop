# On Demand Dev with Docker and WordPress

Docker + WordPress Workshop

- Hosted by [Daniel Olson](https://twitter.com/emaildano)
- In collabration with [Shifter](https://getshifter.io)

### Preparations

- [Install Docker](https://docs.docker.com/install/#supported-platforms)
- [Install Docker Compose](https://docs.docker.com/compose/install/)
- Clone this [repo](https://github.com/getshifter/wceu-workshop)
- If running, shut down the following: MAMP, WAMP, VVV, etc.
- Check to see if Docker is running with command `docker`:

```
$ danielolson : ~/dev/wceu-workshop
$ docker
  
  Usage:	docker COMMAND
  
  A self-sufficient runtime for containers
```

### Warm up your containers

- docker pull wordpress

:question: What does `docker pull` this do?

Docker is a tool designed to run applications as containers. They are small pieces of a larger toolset to create custom applications, products and more.

The official directory for container listings is [Docker Hub](https://hub.docker.com/). In relation to WordPress, Docker Hub is much like the Plugin Directory. It's a place to `pull` resources into your whatever site or project you are working on at that time.

In this instance the command `docker pull` will make a request to download a container from Docker Hub. It will store that container on your local machine for later use.

## Quick Tips

### Useful Docker Commands

| Commands                 | Description                                    |
| ------------------------ | ---------------------------------------------- |
| `docker-compose ps`      | List Containers                                |
| `docker-compose up -d`   | Create and start containers with detached flag |
| `docker-compose stop`    | Stop running containers                        |
| `docker-compose restart` | Restart services                               |
| `docker-compose kill`    | Force stop service containers                  |
| `docker-compose up -d --force-recreate` | Force recreate containers       |
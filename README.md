# On Demand Dev with Docker and WordPress

Docker + WordPress Workshop

- Hosted by [Daniel Olson](https://twitter.com/emaildano)
- Assisted by Zach Gieske
- In collab with [Shifter](https://getshifter.io)

### Preparations

- [Install Docker](https://docs.docker.com/install/#supported-platforms)
- [Install Docker Compose](https://docs.docker.com/compose/install/)
- Clone this [repo](https://github.com/getshifter/wceu-workshop)
- If running, shut down the following: MAMP, WAMP, VVV, etc.
- Check to see if Docker is running with command `docker`
- Check to see if Docker is running with command `docker-compose`

```
$ danielolson : ~/dev/wceu-workshop
$ docker
  
  Usage:	docker COMMAND
  
  A self-sufficient runtime for containers
```

```
$ danielolson : ~/dev/wceu-workshop
$ docker-compose
  
  Define and run multi-container applications with Docker.

  Usage:
    docker-compose [-f <arg>...] [options] [COMMAND] [ARGS...]
    docker-compose -h|--help
```

### Workshop ToC

1. [Docker: Hello World](examples/1-docker-hello-world)
2. [Docker Compose: Hello World](examples/2-docker-compose-hello-world)
3. [Docker Compose: WordPress](examples/3-docker-compose-wordpress)

## Quick Tips

### Useful Docker Commands

| Commands                 | Description                                    |
| ------------------------ | ---------------------------------------------- |
| `docker-compose ps`      | List Containers                                |
| `docker-compose up -d`   | Create and start containers with detached flag |
| `docker-compose stop`    | Stop running containers                        |
| `docker-compose rmi`     | Remove container images                        |
| `docker-compose restart` | Restart services                               |
| `docker-compose kill`    | Force stop service containers                  |
| `docker-compose up -d --force-recreate` | Force recreate containers       |
| `docker stop $(docker ps -a -q)` | Stop all containers                    |
| `docker rm -f $(docker ps -a -q)` | Remove all containers                 |
| `docker rmi -f $(docker images -q)` | Delete all images                   |
| `docker system prune --all` | Remove unused images                        |
| `docker volume rm $(docker volume ls -qf dangling=true)` | Remove volumes |

### Cleanup

| Commands                 | Description                                    |
| ------------------------ | ---------------------------------------------- |
| `docker stop $(docker ps -a -q)` | Stop all containers                    |
| `docker rm -f $(docker ps -a -q)` | Remove all containers                 |
| `docker volume rm $(docker volume ls -qf dangling=true)` | Remove volumes |
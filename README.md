# On Demand Dev with Docker and WordPress

Docker + WordPress Workshop

- Hosted by [Daniel Olson](https://twitter.com/emaildano)
- In collabration with [Shifter](https://getshifter.io)

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
| `docker rm -f $(docker ps -a -q)` | Remove all containers                 |
| `docker stop $(docker ps -a -q)` | Stop all containers                    |
| `docker rmi -f $(docker images -q)` | Delete all images                   |
| `docker system prune --all` | Remove unused images                        |
| `docker volume rm $(docker volume ls -qf dangling=true)` | Remove volumes |

### Workflow Example

1. `docker-compose up -d`
2. `docker-compose stop`
3. `docker rm -f $(docker ps -a -q)`
4. `docker volume rm $(docker volume ls -qf dangling=true)`

## Workshop Guide

1. Install and check requirements
2. Clone this repo
3. CD into project
4. Run build: `docker-compose up -d`
5. View in browser `localhost:8000`
6. Install a plugin, any plugin
7. Navigate to local directory to view local files within Docker container
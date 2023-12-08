# Nexus 3 Set up
## Description
This is a simple set up for Nexus 3. It will create a Nexus 3 instance with a docker repository and a maven group repository.

## Environment Variables
| Variable                | Description                                 | Default Value |
|-------------------------|---------------------------------------------| ------------- |
| MAVEN_PORT              | The port to expose Maven repository on      | 8081 |
| DOCKER_PORT       | The port to expose the docker repository on | 5000 |

## Usage
### Docker
```bash
$ docker run -d -p 8081:8081 -p 5000:5000 --name nexus3 -v nexus-data:/nexus-data -e DOCKER_PORT=5000 -e MAVEN_PORT=8081 nexus3
```

### Docker Compose
```bash
$ docker-compose up -d
```

# mariadb_adminer

This project uses Docker Compose to set up a MariaDB database and Adminer.

## Services

1. **db**: This service uses the MariaDB image. It restarts always and the root password is set to 'example'. The container name is set using the `COMPOSE_PROJECT_NAME` environment variable.

2. **adminer**: This service uses the Adminer image. It restarts always and maps the host port 8081 to the container port 8080. The container name is set using the `COMPOSE_PROJECT_NAME` environment variable.

## How to Run

1. Set your `COMPOSE_PROJECT_NAME` environment variable.
2. Run `docker-compose up` in the terminal.

Please ensure Docker and Docker Compose are installed and running on your machine before attempting to start the services.


In the context of Docker Compose, the COMPOSE_PROJECT_NAME environment variable is used to set the project name, which is prepended to the name of every container started by Docker Compose. This is useful when you're running multiple instances of the same project on the same Docker host to avoid container name conflicts.

To set an environment variable, you can use the export command in Linux or macOS, or the setx command in Windows. For example, to set the COMPOSE_PROJECT_NAME to mariadb_adminer, you would use the following command in a Linux or macOS terminal:
```bash
export COMPOSE_PROJECT_NAME=mariadb_adminer
```

And in Windows:
```bash
setx COMPOSE_PROJECT_NAME mariadb_adminer
```
Remember to replace mariadb_adminer with the actual name you want to use for your project.
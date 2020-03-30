# Docker environment

Docker compose containing most of the tools I need for developing my apps

## Usage

Just execute `docker-compose up -d` and all services will be lifted for you

If you need to view credentials of whatever service has been lifted, review the `docker-compose.yaml` file

`docker-compose down` will terminate them

## Useful commands

Enter the postgres container with `psql`

`$ docker exec -it docker-environment_postgres_1 psql --username=postgres`
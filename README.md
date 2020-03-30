# Docker environment

Docker compose containing most of the tools I need for developing my apps

## Usage

Just execute `docker-compose up -d` and all services will be lifted for you

If you need to view credentials of whatever service has been lifted, review the `docker-compose.yaml` file

`docker-compose down` will terminate them

## Utils

Enter the postgres container with `psql`

`$ docker exec -it docker-environment_postgres_1 psql --username=postgres`

Enter the redis container with `redis-cli`

`$ docker exec -it docker-environment_redis_1 redis-cli`

Save this function to your `.zshrc` (or equivalent) so you can access the compose file from anywhere

```
docker-environment () {
  docker-compose -f {path}/docker-environment/docker-compose.yaml $@
}
```

Replace `{path}` with the path to the `docker-environment` directory

With this you can just `docker-environment up -d` from anywhere (as well as other docker-compose options)
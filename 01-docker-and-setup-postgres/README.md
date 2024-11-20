# Setup Postgres using docker

## Container Concept
- Dockerfile
- Image
- Container

```bash
cd /workspaces/live-demo-data-ai-boostcamp/01-docker-and-setup-postgres/
```

## Pull & Run container
- dockerhub postgres: [https://hub.docker.com/_/postgres](https://hub.docker.com/_/postgres)

```bash
# default docker run on web dockerhub
docker run --name some-postgres -e POSTGRES_PASSWORD=mysecretpassword -d postgres

# change name & add config
docker run --name mypostgres -p 5432:5432 -e POSTGRES_USER=postgres -e POSTGRES_PASSWORD=pg1234 -d postgres:15.9
```

## Cleanup
```bash
# to stop container
docker stop mypostgres

# to remove container
docker rm mypostgres
```
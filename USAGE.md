# Application Usage Guide

This project is a Python HTTP server that runs on port 8000.

## Build the Docker Image

```bash
docker build -t git-docker-app:test .
```

## Run the Application

Start the container and map port 8080 on your computer to port 8000 inside the container.

```bash
docker run -d --name app-test -p 8080:8000 git-docker-app:test
```

## Verify the Application

Send an HTTP request to the application:

```bash
curl http://localhost:8080
```

The response should include the application's health status.

## View Container Logs

```bash
docker logs app-test
```

## Stop and Remove the Container

```bash
docker stop app-test
docker rm app-test
```

## Verify Cleanup

```bash
docker ps -a
```

Confirm that `app-test` no longer appears in the container list.

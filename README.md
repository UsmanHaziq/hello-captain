# Hello Captain - Docker Project

## Overview
This project demonstrates how to create and run a basic Docker image using the Alpine Linux base image. When the container runs, it prints **"Hello, usman!"** to the console and exits.

## Project Structure

```text
hello-captain/
├── Dockerfile
├── compose.yaml
└── README.md
```

## Prerequisites
- Docker Desktop or Docker Engine installed
- Docker running successfully
- Docker Compose (optional, for Compose commands)

## Dockerfile

```dockerfile
FROM alpine:latest
CMD ["echo", "Hello, usman!"]
```

### Explanation
- `FROM alpine:latest`: Uses the latest Alpine Linux image as the base.
- `CMD ["echo", "Hello, usman!"]`: Prints the message when the container runs.

## Build the Docker Image

Open a terminal in the project directory and run:

```bash
docker build -t hello-captain .
```

## Run the Container

```bash
docker run --rm hello-captain
```

### Expected Output

```text
Hello, usman!
```

The container exits after printing the message. The `--rm` option automatically removes the stopped container.

## Run with Docker Compose

Build and run the service:

```bash
docker compose run --build --rm hello-captain
```

Expected output:

```text
Hello, usman!
```

## Troubleshooting

**Image not found:** Build the image before running it:

```bash
docker build -t hello-captain .
```

**Docker daemon error:** Make sure Docker Desktop or Docker Engine is running.

**Incorrect filename:** Ensure the file is named `Dockerfile`, without a `.txt` extension.

## Learning Objectives
- Understand the structure of a Dockerfile.
- Use a base image.
- Build a Docker image.
- Run a container and view its console output.
- Learn basic Docker commands.

https://roadmap.sh/projects/basic-dockerfile

Open your terminal and execute: docker compose up --build

https://roadmap.sh/projects/basic-dockerfile/solutions?u=6ac6764f9195e6b999ec3044

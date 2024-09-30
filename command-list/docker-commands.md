# Useful Docker Commands

- List all containers

    ```bash
    docker ps -a
    ```

- List all running containers

    ```bash
    docker ps
    ```

- List all images

    ```bash
    docker images
    ```

- Inspect a container

    ```bash
    docker inspect $container_name
    ```

- Check if specific container is running

    ```bash
    docker container inspect -f '{{.State.Running}}' $container_name
    ```

- Start a container

    ```bash
    docker start $container_name
    ```

- Stop a container

    ```bash
    docker stop $container_name
    ```

- Inspect specific container parameters

    ```bash
    docker inspect -f '{{range .NetworkSettings.Networks}}{{.EndpointID}}{{end}}' container_name/container_id
    ```

- Remove a container

    ```bash
    docker rm -f container_name/container_id
    ```

- View Stdout and Stderr of a container

    ```bash
    docker logs -f $container_name
    ```

# How to create a custom Redis image

This is a step-by-step guide to creating a custom Redis image in case of fine tuned Redis configurations/customizations/disaster recovery.

## Prerequisites

- Docker

## Steps

1. Create a new directory for your project.

    ```powershell
    mkdir redis-testing
    cd redis-testing
    ```

2. Create a new Dockerfile in the root of your project.

    ```powershell
    cd > Dockerfile
    ```

3. Run a container with the `redis/redis-stack` image.

    ```powershell
    docker run -it --rm --name redis-stack -p 6379:6379 -p 8001:8001 redis/redis-stack:latest
    ```

4. Inspect the container.

    ```powershell
    docker inspect --name redis-stack
    ```

5. Take note of the ENV and the CMD. We will need these later.

6. Stop the container, then export the container.

    ```powershell
    docker stop redis-stack
    docker export --name redis-stack redis-stack-container.tar
    ```

    This will create a file called `redis-stack-container.tar` in the current directory.

7. Add the location of the `redis-stack-container.tar` file to the Dockerfile with COPY to copy it into the container (target the container root directory).

8. Build the image.

    ```powershell
    docker build -t redis-testing .
    ```

9. Run the image.

    ```powershell
    docker run -it --rm --name redis-testing -p 6379:6379 -p 8001:8001 redis-testing
    ```

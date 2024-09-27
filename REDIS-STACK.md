# Redis Testing

This is a simple test project to test the Redis.

## How to run

### Prerequisites

1. Install Docker (WSL is included in the Docker Desktop)

### Steps

We will be installing Redis Stack on Docker.
Redis stack is a complete solution for Redis, including a Redis cluster, a persistence layer, and a GUI.

1. Open a terminal and run the following command:

```bash
# install
$ docker run -d --name redis-stack -p 6379:6379 -p 8001:8001 redis/redis-stack:latest
```

1. Check the containers are running:

    ```bash
    # check example
    docker ps
    ```

2. Enter in the redis-cli

    ```bash
    # enter in redis-cli
    docker exec -it redis-stack redis-cli -h host -p port -a password
    ```

    **NOTE: Please setup credentials and proper security before deploying**
    I dont want data integrity issues when somebody just does a FLUSHALL

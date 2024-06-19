# How to install Redis on Windows

## Method 1: Using Windows Subsystem for Linux (WSL)

1. Enable WSL:

    Open PowerShell as an administrator and run the following command to enable WSL:

    ```sh
    wsl --install
    ```
2. Install a Linux Distribution:

    You can install a Linux distribution like Ubuntu from the Microsoft Store.

3. Update and Install Redis:

    Open your WSL terminal (e.g., Ubuntu) and run the following commands to update your package list and install Redis:

    ```sh
    sudo apt update
    sudo apt install redis-server
    ```

4. Start Redis:

    Start the Redis server with:
    
    ```sh
    sudo service redis-server start
    ```

5. Verify Installation:

    Check if Redis is running by connecting to the Redis server:

    ```sh
    redis-cli
    ```

## Method 2: Using Docker
1. Install Docker Desktop:

    Download and install Docker Desktop from the [Docker website.](https://www.docker.com/products/docker-desktop/)

2. Run Redis Container:

    Open PowerShell or Command Prompt and run the following command to start a Redis container:

    ```
    docker run --name redis -d -p 6379:6379 redis
    ```

3. Verify Installation:

    Connect to the Redis server using the Redis CLI inside the container:

    ```
    docker exec -it redis redis-cli
    ```

## Method 3: Using Memurai (Redis-compatible Windows port)
1. Download Memurai:

    Visit the [Memurai website](https://www.memurai.com) and download the installer for Memurai.

2. Install Memurai:

    Run the installer and follow the installation instructions.

3. Start Memurai:

    Memurai should start automatically. If not, you can start it from the Windows Services Manager.

4. Verify Installation:

    Use the Redis CLI to connect to Memurai:

    ```
    redis-cli -h 127.0.0.1 -p 6379
    ```

## Method 4: Using a Third-Party Port (like tporadowski/redis)

1. Download Redis for Windows:

    Visit the [tporadowski/redis](https://github.com/tporadowski/redis/releases) GitHub repository and download the latest Redis zip file for Windows.

2. Extract and Install:

    Extract the zip file to a directory of your choice (e.g., C:\Redis).

3. Run Redis:

    Open Command Prompt and navigate to the Redis directory:

    ```
    cd C:\Redis
    ```

    Start the Redis server:

    ```
    redis-server.exe
    ```

4. Verify Installation:

    Open another Command Prompt window and connect to the Redis server using the Redis CLI:

    ```
    redis-cli.exe
    ```
# Verification and Basic Usage

Once Redis is installed and running, you can verify the installation and perform basic operations using the Redis CLI:

```
redis-cli
```

In the Redis CLI, you can try the following commands to check if Redis is working correctly:

```
ping
set key "value"
get key
```

These methods provide various ways to install and run Redis on Windows 10, allowing you to choose the one that best fits your environment and requirements.
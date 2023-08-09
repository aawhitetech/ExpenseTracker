# Setting up MS SQL Server in a Local Docker Container

This guide will walk you through the process of running a Microsoft SQL Server instance inside a Docker container on your local machine.
Prerequisites:

**Docker**: Make sure Docker is installed on your machine. If it's not, refer to the [Docker installation guide](https://docs.docker.com/get-docker/).

**Docker Compose**: Ensure Docker Compose is also set up. If needed, follow the [Docker Compose installation guide](https://docs.docker.com/compose/install/).

## Step 1: Navigate to the Docker Directory

Open a terminal or command prompt and navigate to the directory containing the docker-compose.yml file, which should be located in the docker folder:

`cd [PROJECT_ROOT]/docker`

Replace [PROJECT_ROOT] with the actual path to your cloned repository.
## Step 2: Start the SQL Server Docker Container

Run the following command:

`docker-compose up -d`

This command will start the SQL Server container in detached mode. The database configuration, including initializing the expensetracker database, is managed by the [init.sql](../docker/init/init.sql) script. This script is automatically executed when the container starts, ensuring that the database is properly set up.
## Step 3: Verify the SQL Server Container is Running

To confirm that the SQL Server container is up and running:

`docker ps`

Look for the SQL Server container in the list of running containers.
## Step 4: Accessing the Database

With the container running, you can connect to the MS SQL Server instance using your preferred database client. The default credentials are:

    Username: SA
    Password: StrongPassword123
    Host: localhost
    Port: 1433

Make sure to use the expensetracker database, which was initialized by the init.sql script.
## Step 5: Stopping the SQL Server Container

Once you're done, it's a good practice to stop the container:

`docker-compose down`

This will stop and remove the SQL Server container, ensuring that your system resources are not consumed when it's not needed.

Remember, every time you start the container with docker-compose up -d, the init.sql script ensures that the expensetracker database is initialized. However, if there are changes made directly to the database, they might persist across container restarts due to the persistent volume configuration.

If you encounter any issues, refer to the official Docker and SQL Server documentation or seek help from the repository maintainers.
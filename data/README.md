# Docker Entrypoint Initdb

This directory is a linked volume to the `docker-entrypoint-initdb.d` directory of your Docker container. It contains initialization scripts for the Docker entrypoint, which are executed when the container is started for the first time, allowing you to set up the initial state of your database.

## Usage

To use these scripts, place them in this directory. The scripts will be executed in alphabetical order.

## Example

Here is an example of how to use the initialization scripts:

1. Create a script named `init.sql` with the following content:

    ```sql
    CREATE DATABASE mydatabase;
    CREATE USER 'myuser'@'%' IDENTIFIED BY 'mypassword';
    GRANT ALL PRIVILEGES ON mydatabase.* TO 'myuser'@'%';
    ```

2. Place the `init.sql` script in this directory.

3. Build and run your Docker container. The `init.sql` script will be executed, creating the database and user.

## Notes

- The scripts can be in any format supported by your database (e.g., `.sql`, `.sh`).
- Ensure that the scripts have the appropriate permissions to be executed.

For more information, refer to the official Docker documentation on [Initializing a fresh instance](https://hub.docker.com/_/mysql#initializing-a-fresh-instance).


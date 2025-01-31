# Simaju Project

This is the initial setup for a Laravel project using Docker.

## Project Structure

```
/home/ido/Projects/subdomain/simaju/
├── README.md
├── docker-compose.yml
├── Dockerfile
├── src/
│   └── (Laravel source code)
├── php/
│   └── local.ini
├── nginx/
│   └── default.conf
└── data/
    └── initial.sql
```

- **src/**: This directory contains the Laravel source code.
- **data/**: This directory contains the initial SQL file for database setup.
- **php/**: This directory contains the PHP configuration file `local.ini` used to customize PHP settings.
- **nginx/**: This directory contains the Nginx configuration file. 

## Getting Started

1. Clone the repository:
    ```sh
    git clone https://github.com/itpolkesmar/docker-laravel
    cd docker-laravel
    ```

2. Put your laravel source code into `src` directory

3. Don't forget to configure the `.env` file

4. Build and start the Docker containers:
    ```sh
    docker-compose up --build
    ```

5. Access the Laravel application:
    - Open your browser and navigate to `http://localhost`.

## Database Setup

- The initial SQL file located in the `data/` directory will be used to set up the database.

## Useful Commands

- To stop the Docker containers:
    ```sh
    docker-compose down
    ```

- To run artisan commands:
    ```sh
    docker-compose exec app php artisan <command>
    ```
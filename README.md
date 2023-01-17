# WordPress Docker

Simple WordPress development envirement with Docker.

The envirment includes:

- [WordPress and WP CLI](https://hub.docker.com/_/wordpress/)
- [MySQL](https://hub.docker.com/_/mysql/)
- [phpMyAdmin](https://hub.docker.com/r/phpmyadmin/phpmyadmin/)
- [adminer](https://hub.docker.com/_/adminer/)

Contents:

- [Requirements](#requirements)
- [Configuration](#configuration)
- [Installation](#installation)
- [Usage](#usage)

## Requirements

Make sure you have the latest versions of **Docker** and **Docker Compose** installed on your machine.
- [Docker](https://docs.docker.com/engine/install/)
- [Docker compose](https://docs.docker.com/compose/install/)

Clone this repository or copy the files from this repository into a new folder. In the **docker-compose.yml** file you may change the IP address or ports.

## Configuration

Copy the example environment into `.env`

```
cp env.example .env
```

Edit the `.env` file to change the default IP address, MySQL root password and WordPress database name.

## Installation

Open a terminal, navigate to repository root folder and run:

```
docker-compose up -d --build
```

## usage

This creates wp and databse core folders into two separate forlders.

* `database` – used to store and restore database dumps
* `www` – the location of your WordPress core application

At this point You should be able to access the WordPress installation with the configured IP in the browser address. By default it is `http://127.0.0.1` or `lacalhost`.



### phpMyAdmin

You can also visit `http://127.0.0.1:81` to access phpMyAdmin after starting the containers.


### Adminer

You can also visit `http://127.0.0.1:82` to access Adminer after starting the containers.

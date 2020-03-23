# Postgresql & PgAdmin powered by compose


## Requirements:
* docker >= 17.12.0+
* docker-compose

## Quick Start
* Clone or download this repository
* Go inside of directory,  `cd compose-postgres`
* Run this command `docker-compose up -d`

### Set Environment variablse with direnv

Install [direnv](https://direnv.net/) to set up personalize workspace environment variables.

* Run `cp .envrc_vars.example .envrc_vars`
* Set your own variable values
* Run `direnv allow`

Expected output
```bash
$ direnv allow              
direnv: loading .envrc    
direnv: export +PGADMIN_DEFAULT_EMAIL +PGADMIN_DEFAULT_PASSWORD +POSTGRES_PASSWORD +POSTGRES_USER
```

Each time you modify .envrc_vars run `direnv reload`

## Environments
This Compose file contains the following environment variables:

* `POSTGRES_USER` the default value is **postgres**
* `POSTGRES_PASSWORD` the default value is **changeme**
* `PGADMIN_PORT` the default value is **5050**
* `PGADMIN_DEFAULT_EMAIL` the default value is **pgadmin4@pgadmin.org**
* `PGADMIN_DEFAULT_PASSWORD` the default value is **admin**

## Access to postgres: 
* `localhost:5432`
* **Username:** postgres (as a default)
* **Password:** changeme (as a default)

## Access to PgAdmin: 
* **URL:** `http://localhost:5050`
* **Username:** pgadmin4@pgadmin.org (as a default)
* **Password:** admin (as a default)

## Add a new server in PgAdmin:
* **Host name/address** `postgres`
* **Port** `5432`
* **Username** as `POSTGRES_USER`, by default: `postgres`
* **Password** as `POSTGRES_PASSWORD`, by default `changeme`
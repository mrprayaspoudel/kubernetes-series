# GOWT

Sample crud web application project using Golang(http, templates, os, sql), Bootstrap 4, DataTables, MySQL, Docker.

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

### Prerequisites

What things you need to install the software

- Golang, preferably the latest version (1.16).
- MySQL Database
- Docker (optional)

### Installing

1. Clone this repository

```
git clone https://github.com/mrprayaspoudel/kubernetes-series.git
cd kubernetes-series
```

2. Run below command and install dependencies

```
go mod download
```

3. Create database on MySQL

```
CREATE DATABASE gowt;

USE gowt;

CREATE TABLE tools (
  id int(11) NOT NULL AUTO_INCREMENT,
  name varchar(80) COLLATE utf8_unicode_ci DEFAULT NULL,
  category varchar(80) COLLATE utf8_unicode_ci DEFAULT NULL,
  url varchar(255) COLLATE utf8_unicode_ci DEFAULT NULL,
  rating int(11) DEFAULT NULL,
  notes text COLLATE utf8_unicode_ci,
  PRIMARY KEY (id)
) ENGINE=InnoDB DEFAULT CHARSET=utf8 COLLATE=utf8_unicode_ci;
```

4. Create a .env file with the variables listed bellow and change values as needed

```
DATABASE_NAME="gowt"
DATABASE_USERNAME="root"
DATABASE_PASSWORD="Nepal@123"
DATABASE_SERVER="localhost"
DATABASE_PORT="3306"
```

6. Run the application

```
make run
```

## Deployment

1. Create an executable

```
make build
```

2. Run the application

```
./out/bin/gowt
\out\bin\main.exe (Windows)
```

## Create Docker image

1. To build and tag your image locally

```
make docker-build
```

2. To push your image to registry

```
make docker-release
```

## Run Docker image locally

```
make docker-run
```

## Acknowledgments

- This project is in development

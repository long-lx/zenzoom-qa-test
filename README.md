# This guide to setup a development for ap A TODO LIST! AMAZING! with the following packages

```
Laravel 5.5.44
php 7.0.4
nginx 1.10
mysql 5.6
```

# Install Docker and Docker compose
```
## Docker for Mac
https://docs.docker.com/docker-for-mac/install/#install-and-run-docker-for-mac

## Docker for Linux
https://docs.docker.com/install/

## Docker for Windows
https://docs.docker.com/docker-for-windows/install/

## Install Docker compose
ref: https://docs.docker.com/compose/install/
```
# Up development environment

### # Install dependencies
```
docker run --rm -v $(pwd):/app composer/composer install
```

### # Run docker-compose to up development environment
```
$ docker-compose up
```

### # Copy and modify the environment configuration file
```
$ cp .env.example .env
```

### # Setup application key and optimize
```
docker-compose exec app php artisan key:generate
docker-compose exec app php artisan optimize
```

### # Migrate database
```
docker-compose exec app php artisan migrate --seed
```

### # Access from browser
```
http://127.0.0.1:8080
```

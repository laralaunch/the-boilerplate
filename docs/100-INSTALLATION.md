# Installation


## Pre-requisites
[Docker](https://docs.docker.com/engine/install/) (_recommended_) or [php 8.4](https://www.php.net/releases/8.4/en.php) installed locally.

> **ℹ️** How do I quickly install php8.4 on my local? Install [Herd](https://herd.laravel.com). It's easy!

> **⚠️** If you're not planning to use Docker, please make sure to configure [xdebug](https://herd.laravel.com/docs/macos/debugging/xdebug) for code coverage.

## Create project

### Github
Click on the "use this template" button. Clone the created repository on your local.

### GitLab or other
Download source code from the [release](https://github.com/laralaunch/the-boilerplate/releases/).

## Spin-up

### Docker (Recommended)

Run (First time, it will take a couple of minutes as it will build `dev` image from `Dockerfile`):
```
docker compose up -d
```

Inside the application container, run below commands one by one:
```
composer install
cp .env.example .env
php artisan key:generate
touch database/database.sqlite
php artisan migrate
```

Done! Visit http://localhost:8765

### Locally

> Make sure php 8.4 is installed and Xdebug is configured

Run below commands one by one:
```
composer install
cp .env.example .env
php artisan key:generate
touch database/database.sqlite
php artisan migrate
php artisan serve
```

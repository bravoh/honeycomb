# Laravel With Blockchain

My demo application to use Laravel with BlockChain

## Requirements

* PHP 7.2.5 or higher
* HTTP server (for example Apache or NGINX)
* MySQL
* Composer
* Node.js

## Installation

* Clone the repository
* Install dependencies (`composer install --no-dev -o`)
* Run installation command (`php artisan system:install`)
* Configure additional services in `.env` (database or mail, for example)
* Run migrations for database (`php artisan migrate`)
* Head over to your list of crons (`crontab -e`) and add `* * * * * cd /path-to-application && php artisan schedule:run >> /dev/null 2>&1`

*Note that in order for certain features to work properly, the jobs queue needs to be watched. This can be done by either running `php artisan queue:work` or using [Supervisor](https://laravel.com/docs/7.x/queues#supervisor-configuration).*

## Updating

Use the command below to update to the latest version.

```
php artisan budget:update
```

## Docker

You can run Budget using Docker. Spinning it up (`docker-compose up`) will create 3 containers–for MySQL, PHP and NGINX.

*Disclaimer–currently the Docker setup is missing cronjobs and the queue worker.*

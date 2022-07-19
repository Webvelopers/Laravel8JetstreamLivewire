# Laravel 8 Jetstream Livewire

## Create a new Laravel 8 project

🗔 terminal

```bash
 composer create-project laravel/laravel . 8.*
```

## Install Jetstream

🗔 terminal

```bash
composer require laravel/jetstream 1.7.2
php artisan jetstream:install livewire --teams
npm install && npm run dev
```

## Config Laravel Application

🗔 terminal

```bash
code .env
```

✍🏻 .env

```env
APP_NAME="Laravel 8 Jetstream Livewire"
APP_ENV=local
APP_KEY=base64:vt5vyd2EKWFMDmkmppc3qXodN2FgnPxsdRFWEVGIYEI=
APP_DEBUG=true
APP_URL=http://localhost:8000

LOG_CHANNEL=stack
LOG_DEPRECATIONS_CHANNEL=null
LOG_LEVEL=debug

DB_CONNECTION=sqlite

BROADCAST_DRIVER=log
CACHE_DRIVER=file
FILESYSTEM_DRIVER=local
QUEUE_CONNECTION=sync
SESSION_DRIVER=file
SESSION_LIFETIME=120

MEMCACHED_HOST=127.0.0.1

MAIL_MAILER=smtp
MAIL_HOST=smtp.mailtrap.io
MAIL_PORT=587
MAIL_USERNAME=90373441ba81e4
MAIL_PASSWORD=8247686f179633
MAIL_ENCRYPTION=tls
MAIL_FROM_ADDRESS="webmaster@webvelopers.net"
MAIL_FROM_NAME="${APP_NAME}"
```

## Config database and migrations

🗔 terminal

```bash
touch database/database.sqlite
php artisan migrate
```

## Config Jetstream

🗔 terminal

```bash
code config/jetstream.php
```

 ✍🏻 config/jetstream.php

 ```php
 <?php

use Laravel\Jetstream\Features;

return [

    /*
    |--------------------------------------------------------------------------
    | Jetstream Stack
    |--------------------------------------------------------------------------
    |
    | This configuration value informs Jetstream which "stack" you will be
    | using for your application. In general, this value is set for you
    | during installation and will not need to be changed after that.
    |
    */

    'stack' => 'livewire',

    /*
    |--------------------------------------------------------------------------
    | Features
    |--------------------------------------------------------------------------
    |
    | Some of Jetstream's features are optional. You may disable the features
    | by removing them from this array. You're free to only remove some of
    | these features or you can even remove all of these if you need to.
    |
    */

    'features' => [
        Features::profilePhotos(),
        Features::api(),
        Features::teams(),
    ],

];
 ```

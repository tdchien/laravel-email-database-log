# Laravel Email Database Log

A simple database logger for all outgoing emails sent by Laravel website.

## Installation

Laravel Email Database Log can be installed via [composer](http://getcomposer.org) by requiring the `tdchien/laravel-email-database-log` package in your project's `composer.json`.

```json
{
    "require": {
        "tdchien/laravel-email-database-log": "*"
    }
}
```

Next add the service provider and the alias to `app/config/app`.

```php
'providers' => [
    // ...
    tdchien\LaravelEmailDatabaseLog\LaravelEmailDatabaseLogServiceProvider::class,
],
```


Now, run this in terminal:

```bash
php artisan vendor:publish --provider="tdchien\LaravelEmailDatabaseLog\LaravelEmailDatabaseLogServiceProvider" --tag="migrations"

php artisan migrate
```

## Usage

After installation, any email sent by your website will be logged to `email_log` table in the site's database.

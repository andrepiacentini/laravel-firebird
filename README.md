# laravel-firebird

To use this package:

Installation
------------

Install the Firebird PDO driver for PHP.

Install using composer:
```json
composer require andrepiacentini/laravel-firebird
```

**For Laravel 5.1.* support, please look at the [5.1-support](https://github.com/jacquestvanzuydam/laravel-firebird/tree/5.1-support) branch.**

**For Laravel 5.2.* support, please look at the [5.2-sup](https://github.com/jacquestvanzuydam/laravel-firebird/tree/5.2-sup) branch.**

**For Laravel 5.3.* support, please look at the [5.3-support](https://github.com/jacquestvanzuydam/laravel-firebird/tree/5.3-support) branch.**

**For Laravel 5.4.* support, please look at the [5.4-support](https://github.com/jacquestvanzuydam/laravel-firebird/tree/5.4-support) branch.**

**For Laravel 5.5.* support, please look at the [5.5-support](https://github.com/jacquestvanzuydam/laravel-firebird/tree/5.5-support) branch.**

**For Laravel 6.* support, use branch [master](https://github.com/jacquestvanzuydam/laravel-firebird/tree/master) branch.**
=======

Update the `app/config/app.php`, add the service provider:
```json
'Firebird\FirebirdServiceProvider::class'.
```

You can remove the original DatabaseServiceProvider, as the original connection factory has also been extended.

Declare your connection in the database config, using 'firebird' as the
connecion type.
Other keys that are needed:
```php
'firebird' => [
    'driver'   => 'firebird',
    'host'     => env('DB_HOST', 'localhost'),
    'database' => env('DB_DATABASE','/storage/firebird/APPLICATION.FDB'),
    'username' => env('DB_USERNAME', 'sysdba'),
    'password' => env('DB_PASSWORD', 'masterkey'),
    'charset'  => env('DB_CHARSET', 'UTF8'),
],
```

And add to your .env
```
DB_CHARSET=UTF8
```

If necessary, change the UTF8 to any other charset

This package is still in it's infancy and I wouldn't yet recommend using
it for large projects, or without backing up your database regularly.

Any comments or contributions are welcome.

# Use Laravel's blade outside Laravel

[![Latest Version on Packagist](https://img.shields.io/packagist/v/spatie/laravel-blade.svg?style=flat-square)](https://packagist.org/packages/spatie/laravel-blade)
[![Software License](https://img.shields.io/badge/license-MIT-brightgreen.svg?style=flat-square)](LICENSE.md)

### Installation
The package can be installed via Composer by requiring the "50onred/laravel-blade": "1.3" package in your project's composer.json.

```bash
composer require spatie/laravel-blade
```

### Usage

```php
<?php

/*
|--------------------------------------------------------------------------
| Register The Auto Loader
|--------------------------------------------------------------------------
|
| Composer provides a convenient, automatically generated class loader
| for our application. We just need to utilize it! We'll require it
| into the script here so that we do not have to worry about the
| loading of any our classes "manually". Feels great to relax.
|
*/

require 'vendor/autoload.php';

use Spatie\Blade\Blade;

$views = __DIR__ . '/views';
$cache = __DIR__ . '/cache';

$blade = new Blade($views, $cache);
echo $blade->view()->make('hello');
```

You can use all blade features as described in the Laravel 4 documentation:
http://laravel.com/docs/templates#blade-templating

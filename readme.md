# Laravel Active
Laravel Active is a package for Laravel that makes it easy to recognize if the current path or route is active.

## Requirements
- Laravel >=5.5

## Installation
Add Laravel Active to your composer file via the composer require command
```sh
$ composer require imbue/laravel-active
```

> Laravel 5.5 uses Package Auto-Discovery, so does not require you to manually add the ServiceProvider.

Publish the config file to your local config folder
```sh
$ php artisan vendor:publish --tag=laravel-active
```

## Usage
```php
// by path
{{ active('articles') }}
{{ active('articles/*') }}
{{ active(['articles', 'articles/*']) }}
  
// by route name
{{ active('articles.*') }}
{{ active(['articles', 'articles.*']) }}
```

#### Example
```php
<ul class="navbar-nav">
    <li class="nav-item {{ active(['blog', 'blogs/*']) }}">
        <a class="nav-link" href="#">Blog</a>
    </li>
</ul>
```

## Credits
This package is based on the package of [dwightwatson](https://github.com/dwightwatson/active) and stripped down/changed to personal preference.
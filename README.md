# Renovate test

Codebase created with PHP 8.1.13 and Composer 2.5.1

`php` constraint for the project allows PHP 8.1 or newer e.g. PHP 8.2

But one package `laminas/laminas-diactoros` has constraint `^7.3 || ~8.0.0 || ~8.1.0` so PHP 8.2 will cause error
with `composer install`

## Running composer install with PHP 8.2

``` shell
Installing dependencies from lock file (including require-dev)
Verifying lock file contents can be installed on current platform.
Warning: The lock file is not up to date with the latest changes in composer.json. You may be getting outdated dependencies. It is recommended that you run `composer update` or `composer update <package name>`.
Your lock file does not contain a compatible set of packages. Please run composer update.

  Problem 1
    - laminas/laminas-diactoros is locked to version 2.11.3 and an update of this package was not requested.
    - laminas/laminas-diactoros 2.11.3 requires php ^7.3 || ~8.0.0 || ~8.1.0 -> your php version (8.2.1) does not satisfy that requirement.
```

## Running composer install with PHP 8.0

``` shell
Installing dependencies from lock file (including require-dev)
Verifying lock file contents can be installed on current platform.
Warning: The lock file is not up to date with the latest changes in composer.json. You may be getting outdated dependencies. It is recommended that you run `composer update` or `composer update <package name>`.
Your lock file does not contain a compatible set of packages. Please run composer update.

  Problem 1
    - Root composer.json requires php ^8.1 but your php version (8.0.27) does not satisfy that requirement.
```

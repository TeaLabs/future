# Future

This package backports features found in the latest PHP versions.
It provides some of the new features in PHP 5.4+, 5.5+ ,5.6+, 7.0+ and 7.1+ to lower PHP versions.

Most of these features are provided through the following Symfony polyfill packages:-

- `symfony/polyfill-php54` for using the PHP 5.4 functions.
- `symfony/polyfill-php55` for using the PHP 5.5 functions.
- `symfony/polyfill-php56` for using the PHP 5.6 functions.
- `symfony/polyfill-php70` for using the PHP 7.0 functions.
- `symfony/polyfill-php71` for using the PHP 7.1 functions.

## Installation

Requires [Composer](https://getcomposer.org/) to install and load the dependencies.

To install (with composer) run:

    composer require tea/future

Then make sure you `require` Composer's autoloader:

    require 'vendor/autoload.php';


## Usage

The new PHP features are available to you project after calling Composer's autoloader.

For more info on what is available, checkout [symfony-polyfill-phpXX](https://github.com/symfony/polyfill).

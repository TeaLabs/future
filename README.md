# Tea Future

This package backports features found in the latest PHP versions.
It provides some of the new features in PHP 5.4+, 5.5+ ,5.6+, 7.0+ and 7.1+ to lower PHP versions.

> Most of the features are provided by [Symfony Polyfills][] for PHP.

## Installation

Requires [composer][] to install and load the dependencies.

To install, run:

    composer require tea/future

Then [composer][]'s autoloader:

    require 'vendor/autoload.php';


## Features

### 1. PHP 7.0+



lable to your project after calling Composer's autoloader.


- `symfony/polyfill-php54` for using the PHP 5.4 functions.
- `symfony/polyfill-php55` for using the PHP 5.5 functions.
- `symfony/polyfill-php56` for using the PHP 5.6 functions.
- `symfony/polyfill-php70` for using the PHP 7.0 functions.
- `symfony/polyfill-php71` for using the PHP 7.1 functions.

For more info on what is available, checkout [symfony-polyfill-phpXX](https://github.com/symfony/polyfill).


## License

This library is released under the [MIT license](LICENSE).



[composer]: https://getcomposer.org/ "Dependency Manager for PHP"
[symfony polyfills]: https://github.com/symfony/polyfill
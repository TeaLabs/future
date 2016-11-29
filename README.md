# Tea Future

This package back-ports features found in the latest PHP versions.
It provides many of the new features in PHP 5.4+, 5.5+ ,5.6+, 7.0+ and 7.1+ to lower PHP versions.

> Most of these features are provided by [symfony polyfill][] PHP packages.

## Installation

[Composer][] is required to install and load the dependencies.

On your composer managed project, run:

    composer require tea/future

Then load [composer's][composer] autoloader:

    require 'vendor/autoload.php';


## Features

Future provides many of the new PHP functions and classes introduced in PHP 5.4 through to PHP 7.1.

Here are the back-ported features by PHP version:

### PHP 7.1+

Functions:

- [`is_iterable`](http://php.net/is_iterable)

### PHP 7.0+

Functions:

- [`intdiv`](http://php.net/intdiv)
- [`preg_replace_callback_array`](http://php.net/preg_replace_callback_array)
- [`error_clear_last`](http://php.net/error_clear_last)
- `random_bytes` and `random_int` (from [paragonie/random_compat](https://github.com/paragonie/random_compat))

Classes:

- [`*Error` throwable classes](http://php.net/Error)


#### Compatibility notes

To write portable code between PHP5 and PHP7, some care must be taken:
- `\*Error` exceptions must be caught before `\Exception`;
- after calling `error_clear_last()`, the result of `$e = error_get_last()` must be
  verified using `isset($e['message'][0])` instead of `null === $e`.


### PHP 5.6+

Functions:

- [`hash_equals`](http://php.net/hash_equals)  (part of [hash](http://php.net/hash) extension)
- [`ldap_escape`](http://php.net/ldap_escape) (part of [ldap](http://php.net/ldap) extension)


## PHP 5.5+

Functions:

- [`boolval`](http://php.net/boolval)
- [`json_last_error_msg`](http://php.net/json_last_error_msg)
- [`array_column`](http://php.net/array_column)
- [`hash_pbkdf2`](http://php.net/hash_pbkdf2)
- `password_*` functions (from [ircmaxell/password_compat](https://github.com/ircmaxell/password_compat))


## PHP 5.4+

Functions:

- [`trait_exists`](http://php.net/trait_exists)
- [`class_uses`](http://php.net/class_uses)
- [`hex2bin`](http://php.net/hex2bin)
- [`session_register_shutdown`](http://php.net/session_register_shutdown)


## Other

If you only need a polyfill for a specific PHP version, you can simply install the respective
[`symfony/polyfill-phpXX`][symfony polyfill] package.


## License

This library is released under the [MIT license](LICENSE).


[composer]: https://getcomposer.org/ "Dependency Manager for PHP"
[symfony polyfill]: https://github.com/symfony/polyfill "Symfony Polyfill Package"
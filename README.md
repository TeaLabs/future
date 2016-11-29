# Tea Future

This package backports features found in the latest PHP versions.
It provides some of the new features in PHP 5.4+, 5.5+ ,5.6+, 7.0+ and 7.1+ to lower PHP versions.

> Most of the features are provided by [Symfony Polyfills][] for PHP.

## Installation

Requires [composer][] to install and load the dependencies.

After setting up composer, to install future run:

    composer require tea/future

Then load [composer][]'s autoloader:

    require 'vendor/autoload.php';

-----------------------------------------

# Features

## 1. PHP 7.1

- [`is_iterable`](http://php.net/is_iterable)


## 2. PHP 7.0

- [`intdiv`](http://php.net/intdiv)
- [`preg_replace_callback_array`](http://php.net/preg_replace_callback_array)
- [`error_clear_last`](http://php.net/error_clear_last)
- `random_bytes` and `random_int` (from [paragonie/random_compat](https://github.com/paragonie/random_compat))
- [`*Error` throwable classes](http://php.net/Error)

### Compatibility notes

To write portable code between PHP5 and PHP7, some care must be taken:
- `\*Error` exceptions must be caught before `\Exception`;
- after calling `error_clear_last()`, the result of `$e = error_get_last()` must be
  verified using `isset($e['message'][0])` instead of `null === $e`.


## 3. PHP 5.6

- [`hash_equals`](http://php.net/hash_equals)  (part of [hash](http://php.net/hash) extension)
- [`ldap_escape`](http://php.net/ldap_escape) (part of [ldap](http://php.net/ldap) extension)


## 4. PHP 5.5

- [`boolval`](http://php.net/boolval)
- [`json_last_error_msg`](http://php.net/json_last_error_msg)
- [`array_column`](http://php.net/array_column)
- [`hash_pbkdf2`](http://php.net/hash_pbkdf2)
- `password_*` functions (from [ircmaxell/password_compat](https://github.com/ircmaxell/password_compat))


## 5. PHP 5.4

- [`trait_exists`](http://php.net/trait_exists)
- [`class_uses`](http://php.net/class_uses)
- [`hex2bin`](http://php.net/hex2bin)
- [`session_register_shutdown`](http://php.net/session_register_shutdown)

-----------------

You can find more information on the symfony polyfills [here][symfony polyfills].


## License

This library is released under the [MIT license](LICENSE).



[composer]: https://getcomposer.org/ "Dependency Manager for PHP"
[symfony polyfills]: https://github.com/symfony/polyfill
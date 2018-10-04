# Instagram

![instagram](https://cloud.githubusercontent.com/assets/499192/11020990/f0f31dea-8632-11e5-95b1-77e72c7ba271.png)

> An easy-to-use and simple [Instagram](https://www.instagram.com/) package.

```php
use Roketin\Instagram\Instagram;

// Create a new instagram instance.
$instagram = new Instagram('access_token');

// Fetch the user's recent media feed.
$instagram->get();
```

[![Build Status](https://img.shields.io/travis/roketin/instagram/master.svg?style=flat)](https://travis-ci.org/roketin/instagram)
[![StyleCI](https://styleci.io/repos/27216826/shield?style=flat)](https://styleci.io/repos/27216826)
[![Coverage Status](https://img.shields.io/codecov/c/github/roketin/instagram.svg?style=flat)](https://codecov.io/github/roketin/instagram)
[![Latest Version](https://img.shields.io/github/release/roketin/instagram.svg?style=flat)](https://github.com/roketin/instagram/releases)
[![License](https://img.shields.io/packagist/l/roketin/instagram.svg?style=flat)](https://packagist.org/packages/roketin/instagram)

## Installation

Instagram is decoupled from any library sending HTTP requests (like Guzzle), instead it uses an abstraction called [HTTPlug](http://httplug.io) which provides the http layer used to send requests to exchange rate services. This gives you the flexibility to choose what HTTP client and PSR-7 implementation you want to use.

Read more about the benefits of this and about what different HTTP clients you may use in the [HTTPlug documentation](http://docs.php-http.org/en/latest/httplug/users.html). Below is an example using [Guzzle 6](http://docs.guzzlephp.org/en/latest/index.html):

```bash
$ composer require roketin/instagram php-http/message php-http/guzzle6-adapter
```

## Usage

First you need to create a new `roketin\Instagram\Instagram` instance and add your access token. If you don't want to create a Instagram API application you can use [Pixel Union's access token generator](http://instagram.pixelunion.net) for Instagram.

```php
use Roketin\Instagram\Instagram;

$instagram = new Instagram('access_token');
```

To fetch the user's recent media data you may use the `get()` method.

```php
$instagram->get();
```

> **Note:** You can only fetch recent media from the given user's access token.

## License

[MIT](LICENSE) © [Vincent Klaiber](https://vinkla.com)

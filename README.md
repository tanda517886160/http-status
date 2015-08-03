# Httpstatus

[![Latest Version on Packagist](https://img.shields.io/github/release/lukasoppermann/http-status.svg?style=flat-square)](https://github.com/lukasoppermann/http-status/releases)
[![Software License](https://img.shields.io/badge/license-MIT-brightgreen.svg?style=flat-square)](LICENSE.md)
[![Build Status](https://img.shields.io/travis/lukasoppermann/http-status.svg?style=flat-square)](https://travis-ci.org/lukasoppermann/http-status)
[![Total Downloads](https://img.shields.io/packagist/dt/lukasoppermann/http-status.svg?style=flat-square)](https://packagist.org/packages/lukasoppermann/http-status)

**PRE-RELEASE:** This package is currently under development, any feature might be changed or removed until 1.0 is reached.

The Httpstatus package provides an easy and convinent way to retrieve the standard status text (english) for any given HTTP status code. You can also get the HTTP status code for any valid status text. Additionally this package provides all status codes as constants, to use for a better readability of your code (`HTTP_OK` is just much easier to understand than `200`).

## Install

Via Composer

``` bash
$ composer require lukasoppermann/http-status
```

## Usage

``` php
$Httpstatus = new Lukasoppermann\Httpstatus\Httpstatus();
// get status text from code
echo $Httpstatus->text(301); // Moved Permanently
// get the status code by text
echo $Httpstatus->code('Method Not Allowed'); // 405
// using constants
echo $Httpstatus::HTTP_CREATED; // 201
```

## Configure
If you want to localize status texts, you can supply an array when initiating the class. You may overwrite all or just somecodes.

``` php
// add custom texts
$Httpstatus = new Lukasoppermann\Httpstatus\Httpstatus([
    200 => 'Kein Inhalt',
    404 => 'Nicht gefunden',
]);
```


## Available HTTP status codes
Code  |  Message  |  RFC
------------- | ------------- | -------------
100 | Continue | [RFC7231, Section 6.2.1]
101 | Switching Protocols | [RFC7231, Section 6.2.2]
102 | Processing | [RFC2518]
103-199 | *Unassigned* |
200 | OK | [RFC7231, Section 6.3.1]
201 | Created | [RFC7231, Section 6.3.2]
202 | Accepted | [RFC7231, Section 6.3.3]
203 | Non-Authoritative Information | [RFC7231, Section 6.3.4]
204 | No Content | [RFC7231, Section 6.3.5]
205 | Reset Content | [RFC7231, Section 6.3.6]
206 | Partial Content | [RFC7233, Section 4.1]
207 | Multi-Status | [RFC4918]
208 | Already Reported | [RFC5842]
209-225 | *Unassigned* |
226 | IM Used | [RFC3229]
227-299 | *Unassigned* |
300 | Multiple Choices | [RFC7231, Section 6.4.1]
301 | Moved Permanently | [RFC7231, Section 6.4.2]
302 | Found | [RFC7231, Section 6.4.3]
303 | See Other | [RFC7231, Section 6.4.4]
304 | Not Modified | [RFC7232, Section 4.1]
305 | Use Proxy | [RFC7231, Section 6.4.5]
306 | (Unused) | [RFC7231, Section 6.4.6]
307 | Temporary Redirect | [RFC7231, Section 6.4.7]
308 | Permanent Redirect | [RFC7538]
309-399 | *Unassigned* |
400 | Bad Request | [RFC7231, Section 6.5.1]
401 | Unauthorized | [RFC7235, Section 3.1]
402 | Payment Required | [RFC7231, Section 6.5.2]
403 | Forbidden | [RFC7231, Section 6.5.3]
404 | Not Found | [RFC7231, Section 6.5.4]
405 | Method Not Allowed | [RFC7231, Section 6.5.5]
406 | Not Acceptable | [RFC7231, Section 6.5.6]
407 | Proxy Authentication Required | [RFC7235, Section 3.2]
408 | Request Timeout | [RFC7231, Section 6.5.7]
409 | Conflict | [RFC7231, Section 6.5.8]
410 | Gone | [RFC7231, Section 6.5.9]
411 | Length Required | [RFC7231, Section 6.5.10]
412 | Precondition Failed | [RFC7232, Section 4.2]
413 | Payload Too Large | [RFC7231, Section 6.5.11]
414 | URI Too Long | [RFC7231, Section 6.5.12]
415 | Unsupported Media Type | [RFC7231, Section 6.5.13]
416 | Range Not Satisfiable | [RFC7233, Section 4.4]
417 | Expectation Failed | [RFC7231, Section 6.5.14]
418-420 | *Unassigned* |
421 | Misdirected Request | [RFC7540, Section 9.1.2]
422 | Unprocessable Entity | [RFC4918]
423 | Locked | [RFC4918]
424 | Failed Dependency | [RFC4918]
425 | *Unassigned* |
426 | Upgrade Required | [RFC7231, Section 6.5.15]
427 | *Unassigned* |
428 | Precondition Required | [RFC6585]
429 | Too Many Requests | [RFC6585]
430 | *Unassigned* |
431 | Request Header Fields Too Large | [RFC6585]
432-499 | *Unassigned* |
500 | Internal Server Error | [RFC7231, Section 6.6.1]
501 | Not Implemented | [RFC7231, Section 6.6.2]
502 | Bad Gateway | [RFC7231, Section 6.6.3]
503 | Service Unavailable | [RFC7231, Section 6.6.4]
504 | Gateway Timeout | [RFC7231, Section 6.6.5]
505 | HTTP Version Not Supported | [RFC7231, Section 6.6.6]
506 | Variant Also Negotiates | [RFC2295]
507 | Insufficient Storage | [RFC4918]
508 | Loop Detected | [RFC5842]
509 | *Unassigned* |
510 | Not Extended | [RFC2774]
511 | Network Authentication Required | [RFC6585]
512-599 | *Unassigned* |

## Change log

Please see [CHANGELOG](CHANGELOG.md) for more information what has changed recently.

## Testing

``` bash
$ composer test
```

## Contributing

Please see [CONTRIBUTING](CONTRIBUTING.md) for details.

## Security

If you discover any security related issues, please email oppermann.lukas@gmail.com instead of using the issue tracker.

## Credits

- [Lukas Oppermann][link-author]
- [All Contributors][link-contributors]

## License

The MIT License (MIT). Please see [License File](LICENSE.md) for more information.

[link-author]: https://github.com/lukasoppermann
[link-contributors]: ../../contributors

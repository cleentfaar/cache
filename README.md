Cache
=====

Library for quick and easy caching. Supports multiple drivers.

[![Build Status](https://travis-ci.org/treehouselabs/cache.svg?branch=master)](https://travis-ci.org/treehouselabs/cache)
[![Code Coverage](https://scrutinizer-ci.com/g/treehouselabs/cache/badges/coverage.png)](https://scrutinizer-ci.com/g/treehouselabs/cache/)
[![Scrutinizer Code Quality](https://scrutinizer-ci.com/g/treehouselabs/cache/badges/quality-score.png)](https://scrutinizer-ci.com/g/treehouselabs/cache/)

## Installation

```sh
composer require treehouselabs/cache:~1.0
```

## Usage

```php
$driver = new RedisDriver($redis);
$serializer = new JsonSerializer();
$cache = new Cache($driver, $serializer);

$cache->set('foo', 'bar', 60);
$cache->get('foo');
$cache->has('foo');
$cache->remove('foo');
```

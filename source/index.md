---
title: Papi docs

language_tabs:
  - php

toc_footers:
  - <a href='http://github.com/wp-papi/papi'>Fork me on GitHub</a>
  - <a href='http://wp-papi.github.io/'>Papi project site</a>
  - <a href='https://wp-papi.github.io/docs'>Documentation for Papi 2.x</a>

includes:
  - actions
  - api
  - box
  - custom_property
  - page_type
  - properties
  - property_filters
  - setting_filters

search: true
---

# Introduction

**This is the documentation for Papi 1.x**

[**Go to documentation for Papi 2.x**](https://wp-papi.github.io/docs)

So we though why don't use the same approach in WordPress? Papi is  running in production and has been easy to work with when it came to add new fields. Papi don't have any admin user interface where you should add fields, we use classes in PHP, where one class represents one page type and in your class you add all fields you need. It's that easy!

Papi is completely open-source. If you want to help with its development you can submit your suggestions or improvements on in the [Github repository](https://github.com/wp-papi/papi).

## Installation

If you're using Composer to manage WordPress, add Papi to your project's dependencies. Run:

`composer require wp-papi/papi`

Or manually add it to your `composer.json`:

```json
{
  "require": {
    "php": ">=5.3",
    "wordpress": "~4.2",
    "wp-papi/papi": "~1.2"
  }
}
```

# Page Type Directory

Papi does require a directory in your theme, plugin or somewhere in your WordPress site where your page types exists. You can add multiplied directories.

```php
<?php

/**
 * Register page types directory with Papi.
 */

add_filter('papi/settings/directories', function () {
  return __DIR__ . '/includes/page-types';
});
```

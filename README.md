# Moment

A simple PHP API for distributing values based on their probabilities

[![Build Status][ico-build]][link-build]
[![Code Quality][ico-code-quality]][link-code-quality]
[![Code Coverage][ico-code-coverage]][link-code-coverage]
[![Latest Version][ico-version]][link-packagist]
[![PDS Skeleton][ico-pds]][link-pds]

## Installation

The preferred method of installation is via [Composer](http://getcomposer.org/). Run the following command to install the latest version of a package and add it to your project's `composer.json`:

```bash
composer require igorvuckovic/distribution
```

## Usage

```php
use Leaditin\Distribution\Collection;
use Leaditin\Distribution\Distribution;
use Leaditin\Distribution\Element;
use Leaditin\Distribution\Exception\DistributorException;

$collection = new Collection(
    new Element('MALE', 53.25),
    new Element('FEMALE', 46.75)
);

$distribution = new Distribution($collection, 100);

while (true) {
    try {
        echo $distribution->useRandomCode() . PHP_EOL;
    } catch (DistributorException $e) {
        break;
    }
}

```

## Credits

- [All Contributors][link-contributors]

## License

Released under MIT License - see the [License File](LICENSE) for details.


[ico-version]: https://img.shields.io/packagist/v/igorvuckovic/distribution.svg
[ico-build]: https://travis-ci.org/igorvuckovic/distribution.svg?branch=master
[ico-code-coverage]: https://img.shields.io/scrutinizer/coverage/g/igorvuckovic/distribution.svg
[ico-code-quality]: https://img.shields.io/scrutinizer/g/igorvuckovic/distribution.svg
[ico-pds]: https://img.shields.io/badge/pds-skeleton-blue.svg

[link-packagist]: https://packagist.org/packages/igorvuckovic/distribution
[link-build]: https://travis-ci.org/igorvuckovic/distribution
[link-code-coverage]: https://scrutinizer-ci.com/g/igorvuckovic/distribution/code-structure
[link-code-quality]: https://scrutinizer-ci.com/g/igorvuckovic/distribution
[link-pds]: https://github.com/php-pds/skeleton
[link-contributors]: ../../contributors
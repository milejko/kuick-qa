# Kuick QA Toolkit
[![Latest Version](https://img.shields.io/github/release/milejko/kuick-qa-toolkit.svg?cacheSeconds=3600)](https://github.com/milejko/kuick-qa-toolkit/releases)
[![PHP](https://img.shields.io/badge/PHP-8.2%20|%208.3%20|%208.4-blue?logo=php&cacheSeconds=3600)](https://www.php.net)
[![Total Downloads](https://img.shields.io/packagist/dt/kuick/dotenv.svg?cacheSeconds=3600)](https://packagist.org/packages/kuick/qa-toolkit)
[![Software License](https://img.shields.io/badge/license-MIT-brightgreen.svg?cacheSeconds=14400)](LICENSE)

# QA meta-package with popular PHP testing tools
1. Add this section to your composer.json file
```
"scripts": {
    "fix:phpcbf": "phpcbf --standard=PSR12 src tests",
    "test:phpstan": "XDEBUG_MODE=off phpstan --level=9 --no-progress --memory-limit=512M analyse src tests",
    "test:phpcs": "phpcs -n --standard=PSR12 ./src ./tests",
    "test:phpmd": "phpmd src text cleancode,codesize,controversial,design,naming,unusedcode",
    "test:phpunit": "XDEBUG_MODE=coverage phpunit",
    "test:all": [
        "@test:phpcs",
        "@test:phpstan",
        "@test:phpmd",
        "@test:phpunit"
    ]
}
```
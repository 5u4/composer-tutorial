# Composer Tutorial

## How to use

```bash
$ composer require <package-name>
```

```php
<?php

namespace Some\Name\Space;

require_once 'vendor/autoload.php';

use Package;

$test = new Package();

$test->methods();
```

## Uploading

```bash
$ composer init
```

### Autoload

```json
{
    "autoload": {
        "psr-4": {
            "Namespace\\Class\\": "src/location/"
        },
        "files": [
            "src/location/Class.php"
        ]
    }
}
```

## Example

See `src/Greet.php` and `composer.json`

```bash
$ composer require senhung/greet
```

```php
<?php

namespace Some\Name\Space;

require_once 'vendor/autoload.php';

use Senhung\ComposerTutorial\Greet;

$test = new Greet();

/* Hello World! */
$test->greetUser();
```

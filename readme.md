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

## Versioning

| 名称 | 实例 | 描述 |
| ------ | ------ | ------|
| 确切的版本号 | `1.0.2` | 你可以指定包的确切版本。|
| 范围 | `>=1.0` `>=1.0,<2.0` <code>>=1.0,<1.1&#124;>=1.2</code> | 通过使用比较操作符可以指定有效的版本范围。<br/>有效的运算符：`>`、`>=`、`<`、`<=`、`!=`。<br/>你可以定义多个范围，用逗号隔开，这将被视为一个逻辑`AND`处理。一个管道符号<code>&#124;</code>将作为逻辑OR处理。<br/>`AND`的优先级高于`OR`。 |
| 通配符 | `1.0.*` | 你可以使用通配符`*`来指定一种模式。`1.0.*`与`>=1.0,<1.1`是等效的。 |
| 赋值运算符 | `~1.2` | 这对于遵循语义化版本号的项目非常有用。`~1.2`相当于`>=1.2,<2.0`。|


Table content is from [基本用法](https://docs.phpcomposer.com/01-basic-usage.html)

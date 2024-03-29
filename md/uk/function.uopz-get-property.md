---
navigation:
  - function.uopz-get-mock.md: « uopz\_get\_mock
  - function.uopz-get-return.md: uopz\_get\_return »
  - index.md: PHP Manual
  - ref.uopz.md: Функції Uopz
title: uopz\_get\_property
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# uopz\_get\_property

(PECL uopz 5, PECL uopz 6, PECL uopz 7)

uopz\_get\_property — Отримує значення класу або властивість екземпляра

### Опис

```methodsynopsis
uopz_get_property(string $class, string $property): mixed
```

```methodsynopsis
uopz_get_property(object $instance, string $property): mixed
```

Встановлює значення існуючої статичної властивості класу, якщо вказано клас (`class`), або значення існуючої властивості екземпляра, якщо передано екземпляр (`instance`

### Список параметрів

`class`

Назва класу.

`instance`

Примірник об'єкта.

`property`

Ім'я якості.

### Значення, що повертаються

Повертає значення класу або властивість екземпляра, або \*\*`null`\*\*якщо властивість не визначено.

### Приклади

**Приклад #1 Простое использование**uopz\_get\_property()\*\*\*\*

```php
<?php
class Foo {
    private static $staticBar = 10;
    private $bar = 100;
}
$foo = new Foo;
var_dump(uopz_get_property('Foo', 'staticBar'));
var_dump(uopz_get_property($foo, 'bar'));
?>
```

Висновок наведеного прикладу буде схожим на:

```
int(10)
int(100)
```

### Дивіться також

-   [uopz\_set\_property()](function.uopz-set-property.md) \- Встановлює значення існуючої властивості класу чи екземпляра

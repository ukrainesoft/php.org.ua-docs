---
navigation:
  - function.uopz-get-mock.md: « uopzgetmock
  - function.uopz-get-return.md: uopzgetreturn »
  - index.md: PHP Manual
  - ref.uopz.md: Функції Uopz
title: uopzgetproperty
---
# uopzgetproperty

(PECL uopz 5, PECL uopz 6, PECL uopz 7)

uopzgetproperty — Отримує значення класу або властивість екземпляра

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

**Приклад #1 Просте використання **uopzgetproperty()****

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

Результатом виконання цього прикладу буде щось подібне:

```
int(10)
int(100)
```

### Дивіться також

-   [uopzsetproperty()](function.uopz-set-property.md) - Встановлює значення існуючої властивості класу чи екземпляра

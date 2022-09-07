---
navigation:
  - function.uopz-get-static.md: « uopzgetstatic
  - function.uopz-overload.md: uopzoverload »
  - index.md: PHP Manual
  - ref.uopz.md: Функції Uopz
title: uopzimplement
---
# uopzimplement

(PECL uopz 1, PECL uopz 2, PECL uopz 5, PECL uopz 6, PECL uopz 7 < 7.1.0)

uopzimplement — Реалізує інтерфейс під час виконання

### Опис

```methodsynopsis
uopz_implement(string $class, string $interface): bool
```

Робить `class`, що реалізує `interface`

### Список параметрів

`class`

`interface`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Помилки

Починаючи з PHP 7.4.0, **uopzimplements()** викидає [RuntimeException](class.runtimeexception.md), якщо [OPcache](book.opcache.md) включено і запис класу `class` незмінна.

### Приклади

**Приклад #1 Приклад використання **uopzimplement()****

```php
<?php
interface myInterface {}

class myClass {}

uopz_implement(myClass::class, myInterface::class);

var_dump(class_implements(myClass::class));
?>
```

Результат виконання цього прикладу:

```
array(1) {
  ["myInterface"]=>
  string(11) "myInterface"
}
```

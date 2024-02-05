---
navigation:
  - function.uopz-get-static.md: « uopz\_get\_static
  - function.uopz-overload.md: uopz\_overload »
  - index.md: PHP Manual
  - ref.uopz.md: Функції Uopz
title: uopz\_implement
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# uopz\_implement

(PECL uopz 1, PECL uopz 2, PECL uopz 5, PECL uopz 6, PECL uopz 7 < 7.1.0)

uopz\_implement — Реалізує інтерфейс під час виконання

### Опис

```methodsynopsis
uopz_implement(string $class, string $interface): bool
```

Робить `class`, реализующий`interface`

### Список параметрів

`class`

`interface`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Помилки

Починаючи з PHP 7.4.0, **uopz\_implements()** викидає [RuntimeException](class.runtimeexception.md), якщо [OPcache](book.opcache.md) включено і запис класу `class`неизменна.

### Приклади

**Приклад #1 Приклад використання** uopz\_implement()\*\*\*\*

```php
<?php
interface myInterface {}

class myClass {}

uopz_implement(myClass::class, myInterface::class);

var_dump(class_implements(myClass::class));
?>
```

Результат виконання наведеного прикладу:

```
array(1) {
  ["myInterface"]=>
  string(11) "myInterface"
}
```

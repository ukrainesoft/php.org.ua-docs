---
navigation:
  - function.uopz-delete.md: « uopz\_delete
  - function.uopz-flags.md: uopz\_flags »
  - index.md: PHP Manual
  - ref.uopz.md: Функції Uopz
title: uopz\_extend
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# uopz\_extend

(PECL uopz 1, PECL uopz 2, PECL uopz 5, PECL uopz 6, PECL uopz 7 < 7.1.0)

uopz\_extend — Розширити клас під час виконання

### Опис

```methodsynopsis
uopz_extend(string $class, string $parent): bool
```

Розширює поточний клас `class` батьківським `parent`

### Список параметрів

`class`

Назва класу для розширення

`parent`

Назва класу для наслідування

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Помилки

Починаючи з PHP 7.4.0, **uopz\_extends()** викидає [RuntimeException](class.runtimeexception.md), якщо [OPcache](book.opcache.md) включений і запис класу або `class`, либо`parent` (якщо це ознака) незмінні.

### Приклади

**Приклад #1 Приклад використання** uopz\_extend()\*\*\*\*

```php
<?php
class A {}
class B {}

uopz_extend(A::class, B::class);

var_dump(class_parents(A::class));
?>
```

Результат виконання наведеного прикладу:

```
array(1) {
  ["B"]=>
  string(1) "B"
}
```

---
navigation:
  - function.uopz-delete.md: « uopzdelete
  - function.uopz-flags.md: uopzflags »
  - index.md: PHP Manual
  - ref.uopz.md: Функції Uopz
title: uopzextend
---
# uopzextend

(PECL uopz 1, PECL uopz 2, PECL uopz 5, PECL uopz 6, PECL uopz 7 < 7.1.0)

uopzextend — Розширити клас під час виконання

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

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Помилки

Починаючи з PHP 7.4.0, **uopzextends()** викидає [RuntimeException](class.runtimeexception.md), якщо [OPcache](book.opcache.md) включений і запис класу або `class`, або `parent` (якщо це ознака) незмінні.

### Приклади

**Приклад #1 Приклад використання **uopzextend()****

```php
<?php
class A {}
class B {}

uopz_extend(A::class, B::class);

var_dump(class_parents(A::class));
?>
```

Результат виконання цього прикладу:

```
array(1) {
  ["B"]=>
  string(1) "B"
}
```

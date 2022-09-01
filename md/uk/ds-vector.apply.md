---
navigation:
  - ds-vector.allocate.html: '« DsVector::allocate'
  - ds-vector.capacity.html: 'ДсVector::capacity »'
  - index.md: PHP Manual
  - class.ds-vector.html: Вектор
title: 'ДсVector::apply'
---
# ДсVector::apply

(PECL ds >= 1.0.0)

ДсVector::apply — Оновлює всі значення, застосовуючи до них передану callback-функцію

### Опис

```methodsynopsis
public Ds\Vector::apply(callable $callback): void
```

Оновлює всі значення, застосовуючи до них передану `callback`функцію.

### Список параметрів

`callback`

```methodsynopsis
callback(mixed $value): mixed
```

Об'єкт типу [callable](language.types.callable.md)

Callback-функція має повертати нове значення, яке замінить поточне.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **ДсVector::apply()****

```php
<?php
$vector = new \Ds\Vector([1, 2, 3]);
$vector->apply(function($value) { return $value * 2; });

print_r($vector);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Ds\Vector Object
(
    [0] => 2
    [1] => 4
    [2] => 6
)
```

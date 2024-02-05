---
navigation:
  - ds-vector.allocate.md: '« Ds\\Vector::allocate'
  - ds-vector.capacity.md: 'Ds\\Vector::capacity »'
  - index.md: PHP Manual
  - class.ds-vector.md: Ds\\Vector
title: 'Ds\\Vector::apply'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Vector::apply

(PECL ds >= 1.0.0)

Ds\\Vector::apply — Оновлює всі значення, застосовуючи до них передану callback-функцію

### Опис

```methodsynopsis
public Ds\Vector::apply(callable $callback): void
```

Оновлює всі значення, застосовуючи до них передану `callback`\-функцію.

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

**Приклад #1 Приклад використання** Ds\\Vector::apply()\*\*\*\*

```php
<?php
$vector = new \Ds\Vector([1, 2, 3]);
$vector->apply(function($value) { return $value * 2; });

print_r($vector);
?>
```

Висновок наведеного прикладу буде схожим на:

```
Ds\Vector Object
(
    [0] => 2
    [1] => 4
    [2] => 6
)
```

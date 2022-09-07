---
navigation:
  - ds-vector.remove.md: '« DsVector::remove'
  - ds-vector.reversed.md: 'ДсVector::reversed »'
  - index.md: PHP Manual
  - class.ds-vector.md: Вектор
title: 'ДсVector::reverse'
---
# ДсVector::reverse

(PECL ds >= 1.0.0)

ДсVector::reverse — Перевертає поточний вектор

### Опис

```methodsynopsis
public Ds\Vector::reverse(): void
```

Перевертає поточний вектор.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **ДсVector::reverse()****

```php
<?php
$vector = new \Ds\Vector(["a", "b", "c"]);
$vector->reverse();

print_r($vector);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Ds\Vector Object
(
    [0] => c
    [1] => b
    [2] => a
)
```

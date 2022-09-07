---
navigation:
  - ds-vector.capacity.md: '« DsVector::capacity'
  - ds-vector.construct.md: 'ДсVector::construct »'
  - index.md: PHP Manual
  - class.ds-vector.md: Вектор
title: 'ДсVector::clear'
---
# ДсVector::clear

(PECL ds >= 1.0.0)

ДсVector::clear — Видаляє всі значення

### Опис

```methodsynopsis
public Ds\Vector::clear(): void
```

Видаляє всі значення вектора.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **ДсVector::clear()****

```php
<?php
$vector = new \Ds\Vector([1, 2, 3]);
print_r($vector);

$vector->clear();
print_r($vector);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Ds\Vector Object
(
    [0] => 1
    [1] => 2
    [2] => 3
)
Ds\Vector Object
(
)
```

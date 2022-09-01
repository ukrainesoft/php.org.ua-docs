---
navigation:
  - ds-vector.apply.html: '« DsVector::apply'
  - ds-vector.clear.html: 'ДсVector::clear »'
  - index.md: PHP Manual
  - class.ds-vector.html: Вектор
title: 'ДсVector::capacity'
---
# ДсVector::capacity

(PECL ds >= 1.0.0)

ДсVector::capacity — Повертає поточну місткість

### Опис

```methodsynopsis
public Ds\Vector::capacity(): int
```

Повертає поточну місткість.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Поточна місткість.

### Приклади

**Приклад #1 Приклад використання **ДсVector::capacity()****

```php
<?php
$vector = new \Ds\Vector();
var_dump($vector->capacity());

$vector->push(...range(1, 50));
var_dump($vector->capacity());

$vector[] = "a";
var_dump($vector->capacity());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
int(10)
int(50)
int(75)
```

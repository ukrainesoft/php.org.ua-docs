---
navigation:
  - ds-vector.contains.html: '« DsVector::contains'
  - ds-vector.count.html: 'ДсVector::count »'
  - index.html: PHP Manual
  - class.ds-vector.html: Вектор
title: 'ДсVector::copy'
---
# ДсVector::copy

(PECL ds >= 1.0.0)

ДсVector::copy — Повертає поверхневу копію вектора

### Опис

```methodsynopsis
public Ds\Vector::copy(): Ds\Vector
```

Повертає поверхневу копію вектора.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Вектор поверхнева копія.

### Приклади

**Приклад #1 Приклад використання **ДсVector::copy()****

```php
<?php
$a = new \Ds\Vector([1, 2, 3]);
$b = $a->copy();

// Изменение копии не отражается на оригинале
$b->push(4);

print_r($a);
print_r($b);
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
    [0] => 1
    [1] => 2
    [2] => 3
    [3] => 4
)
```

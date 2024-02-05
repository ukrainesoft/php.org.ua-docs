---
navigation:
  - ds-vector.contains.md: '« Ds\\Vector::contains'
  - ds-vector.count.md: 'Ds\\Vector::count »'
  - index.md: PHP Manual
  - class.ds-vector.md: Ds\\Vector
title: 'Ds\\Vector::copy'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Vector::copy

(PECL ds >= 1.0.0)

Ds\\Vector::copy — Повертає поверхневу копію вектора

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

**Приклад #1 Приклад використання** Ds\\Vector::copy()\*\*\*\*

```php
<?php
$a = new \Ds\Vector([1, 2, 3]);
$b = $a->copy();

// Изменение копии не отражается на оригинале
$b->push(4);

print_r($a);
print_r($b);
?>
```

Висновок наведеного прикладу буде схожим на:

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

---
navigation:
  - ds-vector.remove.md: '« Ds\\Vector::remove'
  - ds-vector.reversed.md: 'Ds\\Vector::reversed »'
  - index.md: PHP Manual
  - class.ds-vector.md: Ds\\Vector
title: 'Ds\\Vector::reverse'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Vector::reverse

(PECL ds >= 1.0.0)

Ds\\Vector::reverse — Перевертає поточний вектор

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

**Приклад #1 Приклад використання** Ds\\Vector::reverse()\*\*\*\*

```php
<?php
$vector = new \Ds\Vector(["a", "b", "c"]);
$vector->reverse();

print_r($vector);
?>
```

Висновок наведеного прикладу буде схожим на:

```
Ds\Vector Object
(
    [0] => c
    [1] => b
    [2] => a
)
```

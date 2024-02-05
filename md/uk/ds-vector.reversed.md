---
navigation:
  - ds-vector.reverse.md: '« Ds\\Vector::reverse'
  - ds-vector.rotate.md: 'Ds\\Vector::rotate »'
  - index.md: PHP Manual
  - class.ds-vector.md: Ds\\Vector
title: 'Ds\\Vector::reversed'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Vector::reversed

(PECL ds >= 1.0.0)

Ds\\Vector::reverse — Повертає перегорнуту копію вектора

### Опис

```methodsynopsis
public Ds\Vector::reversed(): Ds\Vector
```

Повертає перегорнуту копію вектора.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Вектор перевернена копія.

> **Зауваження** :
> 
> Поточний вектор не зміниться.

### Приклади

**Пример #1 Пример использования**Ds\\Vector::reversed()\*\*\*\*

```php
<?php
$vector = new \Ds\Vector(["a", "b", "c"]);

print_r($vector->reversed());
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
Ds\Vector Object
(
    [0] => a
    [1] => b
    [2] => c
)
```

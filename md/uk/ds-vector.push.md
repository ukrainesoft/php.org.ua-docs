---
navigation:
  - ds-vector.pop.md: '« Ds\\Vector::pop'
  - ds-vector.reduce.md: 'Ds\\Vector::reduce »'
  - index.md: PHP Manual
  - class.ds-vector.md: Ds\\Vector
title: 'Ds\\Vector::push'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Vector::push

(PECL ds >= 1.0.0)

Ds\\Vector::push — Додає значення до кінця вектора

### Опис

```methodsynopsis
public Ds\Vector::push(mixed ...$values): void
```

Додає значення до кінця вектора.

### Список параметрів

`values`

Значення, що додаються.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Пример #1 Пример использования**Ds\\Vector::push()\*\*\*\*

```php
<?php
$vector = new \Ds\Vector();

$vector->push("a");
$vector->push("b");
$vector->push("c", "d");
$vector->push(...["e", "f"]);

print_r($vector);
?>
```

Висновок наведеного прикладу буде схожим на:

```
Ds\Vector Object
(
    [0] => a
    [1] => b
    [2] => c
    [3] => d
    [4] => e
    [5] => f
)
```

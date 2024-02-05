---
navigation:
  - ds-vector.capacity.md: '« Ds\\Vector::capacity'
  - ds-vector.construct.md: 'Ds\\Vector::\_\_construct »'
  - index.md: PHP Manual
  - class.ds-vector.md: Ds\\Vector
title: 'Ds\\Vector::clear'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Vector::clear

(PECL ds >= 1.0.0)

Ds\\Vector::clear — Видаляє всі значення

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

**Пример #1 Пример использования**Ds\\Vector::clear()\*\*\*\*

```php
<?php
$vector = new \Ds\Vector([1, 2, 3]);
print_r($vector);

$vector->clear();
print_r($vector);
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
)
```

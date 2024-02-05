---
navigation:
  - ds-vector.apply.md: '« Ds\\Vector::apply'
  - ds-vector.clear.md: 'Ds\\Vector::clear »'
  - index.md: PHP Manual
  - class.ds-vector.md: Ds\\Vector
title: 'Ds\\Vector::capacity'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Vector::capacity

(PECL ds >= 1.0.0)

Ds\\Vector::capacity — Повертає поточну місткість

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

**Пример #1 Пример использования**Ds\\Vector::capacity()\*\*\*\*

```php
<?php
$vector = new \Ds\Vector();
var_dump($vector->capacity());

$vector->push(...range(1, 50));
var_dump($vector->capacity());

$vector[] = "a";
var_dump($vector->capacity());
?>
```

Висновок наведеного прикладу буде схожим на:

```
int(10)
int(50)
int(75)
```

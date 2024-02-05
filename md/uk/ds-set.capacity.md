---
navigation:
  - ds-set.allocate.md: '« Ds\\Set::allocate'
  - ds-set.clear.md: 'Ds\\Set::clear »'
  - index.md: PHP Manual
  - class.ds-set.md: Ds\\Set
title: 'Ds\\Set::capacity'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Set::capacity

(PECL ds >= 1.0.0)

Ds\\Set::capacity — Повертає поточну місткість

### Опис

```methodsynopsis
public Ds\Set::capacity(): int
```

Повертає поточну місткість.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Поточна місткість.

### Приклади

**Приклад #1 Приклад використання** Ds\\Set::capacity()\*\*\*\*

```php
<?php
$set = new \Ds\Set();
var_dump($set->capacity());

$set->add(...range(1, 50));
var_dump($set->capacity());
?>
```

Висновок наведеного прикладу буде схожим на:

```
int(16)
int(64)
```

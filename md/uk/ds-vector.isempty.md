---
navigation:
  - ds-vector.insert.md: '« Ds\\Vector::insert'
  - ds-vector.join.md: 'Ds\\Vector::join »'
  - index.md: PHP Manual
  - class.ds-vector.md: Ds\\Vector
title: 'Ds\\Vector::isEmpty'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Vector::isEmpty

(PECL ds >= 1.0.0)

Ds\\Vector::isEmpty — Перевіряє, чи порожній вектор

### Опис

```methodsynopsis
public Ds\Vector::isEmpty(): bool
```

Перевіряє, чи вектор порожній.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`**, якщо вектор порожній, **`false`** в іншому випадку.

### Приклади

**Приклад #1 Приклад використання** Ds\\Vector::isEmpty()\*\*\*\*

```php
<?php
$a = new \Ds\Vector([1, 2, 3]);
$b = new \Ds\Vector();

var_dump($a->isEmpty());
var_dump($b->isEmpty());
?>
```

Висновок наведеного прикладу буде схожим на:

```
bool(false)
bool(true)
```

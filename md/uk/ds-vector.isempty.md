---
navigation:
  - ds-vector.insert.md: '« DsVector::insert'
  - ds-vector.join.md: 'ДсVector::join »'
  - index.md: PHP Manual
  - class.ds-vector.md: Вектор
title: 'ДсVector::isEmpty'
---
# ДсVector::isEmpty

(PECL ds >= 1.0.0)

ДсVector::isEmpty — Перевіряє, чи порожній вектор

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

**Приклад #1 Приклад використання **ДсVector::isEmpty()****

```php
<?php
$a = new \Ds\Vector([1, 2, 3]);
$b = new \Ds\Vector();

var_dump($a->isEmpty());
var_dump($b->isEmpty());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
bool(false)
bool(true)
```

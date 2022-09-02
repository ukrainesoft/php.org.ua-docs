---
navigation:
  - ds-vector.jsonserialize.md: '« DsVector::jsonSerialize'
  - ds-vector.map.md: 'ДсVector::map »'
  - index.md: PHP Manual
  - class.ds-vector.md: Вектор
title: 'ДсVector::last'
---
# ДсVector::last

(PECL ds >= 1.0.0)

ДсVector::last — Повертає останнє значення вектора

### Опис

```methodsynopsis
public Ds\Vector::last(): mixed
```

Повертає останнє значення вектора.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Останній елемент вектор.

### Помилки

Викидає виняток [UnderflowException](class.underflowexception.md)якщо вектор порожній.

### Приклади

**Приклад #1 Приклад використання **ДсVector::last()****

```php
<?php
$vector = new \Ds\Vector([1, 2, 3]);
var_dump($vector->last());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
int(3)
```

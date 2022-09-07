---
navigation:
  - ds-vector.find.md: '« DsVector::find'
  - ds-vector.get.md: 'ДсVector::get »'
  - index.md: PHP Manual
  - class.ds-vector.md: Вектор
title: 'ДсVector::first'
---
# ДсVector::first

(PECL ds >= 1.0.0)

ДсVector::first — Повертає перший елемент вектора

### Опис

```methodsynopsis
public Ds\Vector::first(): mixed
```

Повертає перший елемент вектор.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Перший елемент вектор.

### Помилки

Викидає виняток [UnderflowException](class.underflowexception.md)якщо вектор порожній.

### Приклади

**Приклад #1 Приклад використання **ДсVector::first()****

```php
<?php
$vector = new \Ds\Vector([1, 2, 3]);
var_dump($vector->first());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
int(1)
```

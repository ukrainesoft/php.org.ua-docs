---
navigation:
  - ds-vector.set.md: '« DsVector::set'
  - ds-vector.slice.md: 'ДсVector::slice »'
  - index.md: PHP Manual
  - class.ds-vector.md: Вектор
title: 'ДсVector::shift'
---
# ДсVector::shift

(PECL ds >= 1.0.0)

ДсVector::shift — Видаляє та повертає перше значення

### Опис

```methodsynopsis
public Ds\Vector::shift(): mixed
```

Видаляє та повертає перше значення.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Перше віддалене значення.

### Помилки

Викидає виняток [UnderflowException](class.underflowexception.md)якщо вектор порожній.

### Приклади

**Приклад #1 Приклад використання **ДсVector::shift()****

```php
<?php
$vector = new \Ds\Vector(["a", "b", "c"]);

var_dump($vector->shift());
var_dump($vector->shift());
var_dump($vector->shift());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
string(1) "a"
string(1) "b"
string(1) "c"
```

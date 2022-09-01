---
navigation:
  - ds-vector.merge.html: '« DsVector::merge'
  - ds-vector.push.html: 'ДсVector::push »'
  - index.md: PHP Manual
  - class.ds-vector.html: Вектор
title: 'ДсVector::pop'
---
# ДсVector::pop

(PECL ds >= 1.0.0)

ДсVector::pop — Видаляє та повертає останнє значення

### Опис

```methodsynopsis
public Ds\Vector::pop(): mixed
```

Видаляє та повертає останнє значення.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Останнє віддалене значення.

### Помилки

Викидає виняток [UnderflowException](class.underflowexception.md)якщо вектор порожній.

### Приклади

**Приклад #1 Приклад використання **ДсVector::pop()****

```php
<?php
$vector = new \Ds\Vector([1, 2, 3]);

var_dump($vector->pop());
var_dump($vector->pop());
var_dump($vector->pop());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
int(3)
int(2)
int(1)
```

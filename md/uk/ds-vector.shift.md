---
navigation:
  - ds-vector.set.md: '« Ds\\Vector::set'
  - ds-vector.slice.md: 'Ds\\Vector::slice »'
  - index.md: PHP Manual
  - class.ds-vector.md: Ds\\Vector
title: 'Ds\\Vector::shift'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Vector::shift

(PECL ds >= 1.0.0)

Ds\\Vector::shift — Видаляє та повертає перше значення

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

**Пример #1 Пример использования**Ds\\Vector::shift()\*\*\*\*

```php
<?php
$vector = new \Ds\Vector(["a", "b", "c"]);

var_dump($vector->shift());
var_dump($vector->shift());
var_dump($vector->shift());
?>
```

Висновок наведеного прикладу буде схожим на:

```
string(1) "a"
string(1) "b"
string(1) "c"
```

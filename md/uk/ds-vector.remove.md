---
navigation:
  - ds-vector.reduce.md: '« Ds\\Vector::reduce'
  - ds-vector.reverse.md: 'Ds\\Vector::reverse »'
  - index.md: PHP Manual
  - class.ds-vector.md: Ds\\Vector
title: 'Ds\\Vector::remove'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Vector::remove

(PECL ds >= 1.0.0)

Ds\\Vector::remove — Видаляє та повертає значення за індексом

### Опис

```methodsynopsis
public Ds\Vector::remove(int $index): mixed
```

Видаляє та повертає значення за індексом.

### Список параметрів

`index`

Індекс, яким необхідно видалити значення.

### Значення, що повертаються

Віддалене значення.

### Помилки

Викидає виняток [OutOfRangeException](class.outofrangeexception.md)якщо індекс некоректний.

### Приклади

**Приклад #1 Приклад використання** Ds\\Vector::remove()\*\*\*\*

```php
<?php
$vector = new \Ds\Vector(["a", "b", "c"]);

var_dump($vector->remove(1));
var_dump($vector->remove(0));
var_dump($vector->remove(0));
?>
```

Висновок наведеного прикладу буде схожим на:

```
string(1) "b"
string(1) "a"
string(1) "c"
```

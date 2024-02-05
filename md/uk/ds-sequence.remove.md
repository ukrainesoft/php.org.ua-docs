---
navigation:
  - ds-sequence.reduce.md: '« Ds\\Sequence::reduce'
  - ds-sequence.reverse.md: 'Ds\\Sequence::reverse »'
  - index.md: PHP Manual
  - class.ds-sequence.md: Ds\\Sequence
title: 'Ds\\Sequence::remove'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Sequence::remove

(PECL ds >= 1.0.0)

Ds\\Sequence::remove — Видаляє та повертає значення за індексом

### Опис

```methodsynopsis
abstract public Ds\Sequence::remove(int $index): mixed
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

**Пример #1 Пример использования**Ds\\Sequence::remove()\*\*\*\*

```php
<?php
$sequence = new \Ds\Vector(["a", "b", "c"]);

var_dump($sequence->remove(1));
var_dump($sequence->remove(0));
var_dump($sequence->remove(0));
?>
```

Висновок наведеного прикладу буде схожим на:

```
string(1) "b"
string(1) "a"
string(1) "c"
```

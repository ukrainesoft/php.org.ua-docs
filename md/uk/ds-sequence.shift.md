---
navigation:
  - ds-sequence.set.md: '« Ds\\Sequence::set'
  - ds-sequence.slice.md: 'Ds\\Sequence::slice »'
  - index.md: PHP Manual
  - class.ds-sequence.md: Ds\\Sequence
title: 'Ds\\Sequence::shift'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Sequence::shift

(PECL ds >= 1.0.0)

Ds\\Sequence::shift — Видаляє та повертає перше значення

### Опис

```methodsynopsis
abstract public Ds\Sequence::shift(): mixed
```

Видаляє та повертає перше значення.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Перше віддалене значення.

### Помилки

Викидає виняток [UnderflowException](class.underflowexception.md)якщо колекція порожня.

### Приклади

**Пример #1 Пример использования**Ds\\Sequence::shift()\*\*\*\*

```php
<?php
$sequence = new \Ds\Vector(["a", "b", "c"]);

var_dump($sequence->shift());
var_dump($sequence->shift());
var_dump($sequence->shift());
?>
```

Висновок наведеного прикладу буде схожим на:

```
string(1) "a"
string(1) "b"
string(1) "c"
```

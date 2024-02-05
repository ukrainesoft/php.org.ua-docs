---
navigation:
  - ds-sequence.merge.md: '« Ds\\Sequence::merge'
  - ds-sequence.push.md: 'Ds\\Sequence::push »'
  - index.md: PHP Manual
  - class.ds-sequence.md: Ds\\Sequence
title: 'Ds\\Sequence::pop'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Sequence::pop

(PECL ds >= 1.0.0)

Ds\\Sequence::pop — Видаляє та повертає останнє значення

### Опис

```methodsynopsis
abstract public Ds\Sequence::pop(): mixed
```

Видаляє та повертає останнє значення.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Останнє віддалене значення.

### Помилки

Викидає виняток [UnderflowException](class.underflowexception.md)якщо колекція порожня.

### Приклади

**Пример #1 Пример использования**Ds\\Sequence::pop()\*\*\*\*

```php
<?php
$sequence = new \Ds\Vector([1, 2, 3]);

var_dump($sequence->pop());
var_dump($sequence->pop());
var_dump($sequence->pop());
?>
```

Висновок наведеного прикладу буде схожим на:

```
int(3)
int(2)
int(1)
```

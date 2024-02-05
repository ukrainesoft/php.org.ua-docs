---
navigation:
  - ds-sequence.join.md: '« Ds\\Sequence::join'
  - ds-sequence.map.md: 'Ds\\Sequence::map »'
  - index.md: PHP Manual
  - class.ds-sequence.md: Ds\\Sequence
title: 'Ds\\Sequence::last'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Sequence::last

(PECL ds >= 1.0.0)

Ds\\Sequence::last — Повертає останнє значення колекції

### Опис

```methodsynopsis
abstract public Ds\Sequence::last(): mixed
```

Повертає останнє значення колекції.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Останній елемент колекції.

### Помилки

Викидає виняток [UnderflowException](class.underflowexception.md)якщо колекція порожня.

### Приклади

**Пример #1 Пример использования**Ds\\Sequence::last()\*\*\*\*

```php
<?php
$sequence = new \Ds\Vector([1, 2, 3]);
var_dump($sequence->last());
?>
```

Висновок наведеного прикладу буде схожим на:

```
int(3)
```

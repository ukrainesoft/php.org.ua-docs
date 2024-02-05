---
navigation:
  - ds-sequence.find.md: '« Ds\\Sequence::find'
  - ds-sequence.get.md: 'Ds\\Sequence::get »'
  - index.md: PHP Manual
  - class.ds-sequence.md: Ds\\Sequence
title: 'Ds\\Sequence::first'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Sequence::first

(PECL ds >= 1.0.0)

Ds\\Sequence::first — Повертає перший елемент колекції

### Опис

```methodsynopsis
abstract public Ds\Sequence::first(): mixed
```

Повертає перший елемент колекції.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Перший елемент колекції.

### Помилки

Викидає виняток [UnderflowException](class.underflowexception.md)якщо колекція порожня.

### Приклади

**Пример #1 Пример использования**Ds\\Sequence::first()\*\*\*\*

```php
<?php
$sequence = new \Ds\Vector([1, 2, 3]);
var_dump($sequence->first());
?>
```

Висновок наведеного прикладу буде схожим на:

```
int(1)
```

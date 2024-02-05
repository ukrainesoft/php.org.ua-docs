---
navigation:
  - ds-set.jsonserialize.md: '« Ds\\Set::jsonSerialize'
  - ds-set.merge.md: 'Ds\\Set::merge »'
  - index.md: PHP Manual
  - class.ds-set.md: Ds\\Set
title: 'Ds\\Set::last'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Set::last

(PECL ds >= 1.0.0)

Ds\\Set::last — Повертає останнє значення колекції

### Опис

```methodsynopsis
public Ds\Set::last(): mixed
```

Повертає останнє значення колекції.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Останній елемент колекції.

### Помилки

Викидає виняток [UnderflowException](class.underflowexception.md)якщо колекція порожня.

### Приклади

**Приклад #1 Приклад використання** Ds\\Set::last()\*\*\*\*

```php
<?php
$set = new \Ds\Set([1, 2, 3]);
var_dump($set->last());
?>
```

Висновок наведеного прикладу буде схожим на:

```
int(3)
```

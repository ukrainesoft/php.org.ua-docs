---
navigation:
  - ds-set.filter.md: '« Ds\\Set::filter'
  - ds-set.get.md: 'Ds\\Set::get »'
  - index.md: PHP Manual
  - class.ds-set.md: Ds\\Set
title: 'Ds\\Set::first'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Set::first

(PECL ds >= 1.0.0)

Ds\\Set::first — Повертає перший елемент колекції

### Опис

```methodsynopsis
public Ds\Set::first(): mixed
```

Повертає перший елемент колекції.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Перший елемент колекції.

### Помилки

Викидає виняток [UnderflowException](class.underflowexception.md)якщо колекція порожня.

### Приклади

**Приклад #1 Приклад використання** Ds\\Set::first()\*\*\*\*

```php
<?php
$set = new \Ds\Set([1, 2, 3]);
var_dump($set->first());
?>
```

Висновок наведеного прикладу буде схожим на:

```
int(1)
```

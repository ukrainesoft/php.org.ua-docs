---
navigation:
  - ds-collection.copy.md: '« Ds\\Collection::copy'
  - ds-collection.toarray.md: 'Ds\\Collection::toArray »'
  - index.md: PHP Manual
  - class.ds-collection.md: Ds\\Collection
title: 'Ds\\Collection::isEmpty'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Collection::isEmpty

(PECL ds >= 1.0.0)

Ds\\Collection::isEmpty — Перевіряє, чи колекція порожня.

### Опис

```methodsynopsis
public Ds\Collection::isEmpty(): bool
```

Перевіряє, чи колекція порожня.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`**, если коллекция пуста, и\*\*`false`\*\* в іншому випадку.

### Приклади

**Приклад #1 Приклад**Ds\\Collection::isEmpty()\*\*\*\*

```php
<?php
$a = new \Ds\Vector([1, 2, 3]);
$b = new \Ds\Vector();

var_dump($a->isEmpty());
var_dump($b->isEmpty());
?>
```

Висновок наведеного прикладу буде схожим на:

```
bool(false)
bool(true)
```

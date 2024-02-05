---
navigation:
  - ds-set.intersect.md: '« Ds\\Set::intersect'
  - ds-set.join.md: 'Ds\\Set::join »'
  - index.md: PHP Manual
  - class.ds-set.md: Ds\\Set
title: 'Ds\\Set::isEmpty'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Set::isEmpty

(PECL ds >= 1.0.0)

Ds\\Set::isEmpty — Перевіряє, чи колекція порожня.

### Опис

```methodsynopsis
public Ds\Set::isEmpty(): bool
```

Перевіряє, чи колекція порожня.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`**, если коллекция пуста,**`false`** в іншому випадку.

### Приклади

**Пример #1 Пример использования**Ds\\Set::isEmpty()\*\*\*\*

```php
<?php
$a = new \Ds\Set([1, 2, 3]);
$b = new \Ds\Set();

var_dump($a->isEmpty());
var_dump($b->isEmpty());
?>
```

Висновок наведеного прикладу буде схожим на:

```
bool(false)
bool(true)
```

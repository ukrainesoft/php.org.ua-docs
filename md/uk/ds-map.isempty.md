---
navigation:
  - ds-map.intersect.md: '« DsMap::intersect'
  - ds-map.jsonserialize.md: 'ДсMap::jsonSerialize »'
  - index.md: PHP Manual
  - class.ds-map.md: Коллекция пар ключ-значение
title: 'ДсMap::isEmpty'
---
# ДсMap::isEmpty

(PECL ds >= 1.0.0)

ДсMap::isEmpty — Перевіряє, чи порожня колекція

### Опис

```methodsynopsis
public Ds\Map::isEmpty(): bool
```

Перевіряє, чи колекція порожня.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`**, якщо колекція порожня, та **`false`** в іншому випадку.

### Приклади

**Приклад #1 Приклад використання **ДсMap::isEmpty()****

```php
<?php
$a = new \Ds\Map(["a" => 1, "b" => 2, "c" => 3]);
$b = new \Ds\Map();

var_dump($a->isEmpty());
var_dump($b->isEmpty());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
bool(false)
bool(true)
```

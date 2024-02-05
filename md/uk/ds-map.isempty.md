---
navigation:
  - ds-map.intersect.md: '« Ds\\Map::intersect'
  - ds-map.jsonserialize.md: 'Ds\\Map::jsonSerialize »'
  - index.md: PHP Manual
  - class.ds-map.md: Ds\\Map
title: 'Ds\\Map::isEmpty'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Map::isEmpty

(PECL ds >= 1.0.0)

Ds\\Map::isEmpty — Перевіряє, чи порожня колекція

### Опис

```methodsynopsis
public Ds\Map::isEmpty(): bool
```

Перевіряє, чи колекція порожня.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`**, если коллекция пуста, и\*\*`false`\*\* в іншому випадку.

### Приклади

**Приклад #1 Приклад використання** Ds\\Map::isEmpty()\*\*\*\*

```php
<?php
$a = new \Ds\Map(["a" => 1, "b" => 2, "c" => 3]);
$b = new \Ds\Map();

var_dump($a->isEmpty());
var_dump($b->isEmpty());
?>
```

Висновок наведеного прикладу буде схожим на:

```
bool(false)
bool(true)
```

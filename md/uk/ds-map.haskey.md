---
navigation:
  - ds-map.get.md: '« Ds\\Map::get'
  - ds-map.hasvalue.md: 'Ds\\Map::hasValue »'
  - index.md: PHP Manual
  - class.ds-map.md: Ds\\Map
title: 'Ds\\Map::hasKey'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Map::hasKey

(PECL ds >= 1.0.0)

Ds\\Map::hasKey — Перевіряє, чи колекція містить заданий ключ

### Опис

```methodsynopsis
public Ds\Map::hasKey(mixed $key): bool
```

Перевіряє, чи колекція містить заданий ключ.

### Список параметрів

`key`

Ключ, що перевіряється.

### Значення, що повертаються

Повертає **`true`**, если ключ найден, иначе\*\*`false`\*\*

### Приклади

**Приклад #1 Приклад використання** Ds\\Map::hasKey()\*\*\*\*

```php
<?php
$map = new \Ds\Map(["a" => 1, "b" => 2, "c" => 3]);

var_dump($map->hasKey("a")); // true
var_dump($map->hasKey("e")); // false
?>
```

Висновок наведеного прикладу буде схожим на:

```
bool(true)
bool(false)
```

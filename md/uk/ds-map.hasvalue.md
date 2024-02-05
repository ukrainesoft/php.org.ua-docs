---
navigation:
  - ds-map.haskey.md: '« Ds\\Map::hasKey'
  - ds-map.intersect.md: 'Ds\\Map::intersect »'
  - index.md: PHP Manual
  - class.ds-map.md: Ds\\Map
title: 'Ds\\Map::hasValue'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Map::hasValue

(PECL ds >= 1.0.0)

Ds\\Map::hasValue — Перевіряє, чи колекція містить задане значення

### Опис

```methodsynopsis
public Ds\Map::hasValue(mixed $value): bool
```

Перевіряє, чи колекція містить задане значення.

### Список параметрів

`value`

Значення для перевірки.

### Значення, що повертаються

Повертає **`true`**, если ключ найден, иначе\*\*`false`\*\*

### Приклади

**Пример #1 Пример использования**Ds\\Map::hasValue()\*\*\*\*

```php
<?php
$map = new \Ds\Map(["a" => 1, "b" => 2, "c" => 3]);

var_dump($map->hasValue(1)); // true
var_dump($map->hasValue(4)); // false
?>
```

Висновок наведеного прикладу буде схожим на:

```
bool(true)
bool(false)
```

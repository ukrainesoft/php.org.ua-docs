---
navigation:
  - ds-map.apply.md: '« Ds\\Map::apply'
  - ds-map.clear.md: 'Ds\\Map::clear »'
  - index.md: PHP Manual
  - class.ds-map.md: Ds\\Map
title: 'Ds\\Map::capacity'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Map::capacity

(PECL ds >= 1.0.0)

Ds\\Map::capacity — Повертає поточну місткість

### Опис

```methodsynopsis
public Ds\Map::capacity(): int
```

Повертає поточну місткість.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Поточна місткість.

### Приклади

**Пример #1 Пример использования**Ds\\Map::capacity()\*\*\*\*

```php
<?php
$map = new \Ds\Map();
var_dump($map->capacity());
?>
```

Висновок наведеного прикладу буде схожим на:

```
int(16)
```

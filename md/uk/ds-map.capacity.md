---
navigation:
  - ds-map.apply.html: '« DsMap::apply'
  - ds-map.clear.html: 'ДсMap::clear »'
  - index.md: PHP Manual
  - class.ds-map.html: Коллекция пар ключ-значение
title: 'ДсMap::capacity'
---
# ДсMap::capacity

(PECL ds >= 1.0.0)

ДсMap::capacity — Повертає поточну місткість

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

**Приклад #1 Приклад використання **ДсMap::capacity()****

```php
<?php
$map = new \Ds\Map();
var_dump($map->capacity());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
int(16)
```

---
navigation:
  - ds-map.get.md: '« DsMap::get'
  - ds-map.hasvalue.md: 'ДсMap::hasValue »'
  - index.md: PHP Manual
  - class.ds-map.md: Коллекция пар ключ-значение
title: 'ДсMap::hasKey'
---
# ДсMap::hasKey

(PECL ds >= 1.0.0)

ДсMap::hasKey — Перевіряє, чи колекція містить заданий ключ

### Опис

```methodsynopsis
public Ds\Map::hasKey(mixed $key): bool
```

Перевіряє, чи колекція містить заданий ключ.

### Список параметрів

`key`

Ключ, що перевіряється.

### Значення, що повертаються

Повертає \*\*`true`\*\*якщо ключ знайдений, інакше **`false`**

### Приклади

**Приклад #1 Приклад використання **ДсMap::hasKey()****

```php
<?php
$map = new \Ds\Map(["a" => 1, "b" => 2, "c" => 3]);

var_dump($map->hasKey("a")); // true
var_dump($map->hasKey("e")); // false
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
bool(true)
bool(false)
```

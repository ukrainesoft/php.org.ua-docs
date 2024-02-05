---
navigation:
  - ds-map.capacity.md: '« Ds\\Map::capacity'
  - ds-map.construct.md: 'Ds\\Map::\_\_construct »'
  - index.md: PHP Manual
  - class.ds-map.md: Ds\\Map
title: 'Ds\\Map::clear'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Map::clear

(PECL ds >= 1.0.0)

Ds\\Map::clear — Видаляє всі значення з колекції

### Опис

```methodsynopsis
public Ds\Map::clear(): void
```

Видаляє всі значення колекції.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання** Ds\\Map::clear()\*\*\*\*

```php
<?php
$map = new \Ds\Map([
    "a" => 1,
    "b" => 2,
    "c" => 3,
]);
print_r($map);

$map->clear();
print_r($map);
?>
```

Висновок наведеного прикладу буде схожим на:

```
Ds\Map Object
(
    [0] => Ds\Pair Object
        (
            [key] => a
            [value] => 1
        )

    [1] => Ds\Pair Object
        (
            [key] => b
            [value] => 2
        )

    [2] => Ds\Pair Object
        (
            [key] => c
            [value] => 3
        )

)
Ds\Map Object
(
)
```

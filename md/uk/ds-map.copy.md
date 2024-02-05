---
navigation:
  - ds-map.construct.md: '« Ds\\Map::\_\_construct'
  - ds-map.count.md: 'Ds\\Map::count »'
  - index.md: PHP Manual
  - class.ds-map.md: Ds\\Map
title: 'Ds\\Map::copy'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Map::copy

(PECL ds >= 1.0.0)

Ds\\Map::copy — Повертає поверхневу копію колекції

### Опис

```methodsynopsis
public Ds\Map::copy(): Ds\Map
```

Повертає поверхневу копію колекції.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Колекція поверхнева копія.

### Приклади

**Пример #1 Пример использования**Ds\\Map::copy()\*\*\*\*

```php
<?php
$map = new \Ds\Map([
    "a" => 1,
    "b" => 2,
    "c" => 3,
]);

print_r($map->copy());
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
```

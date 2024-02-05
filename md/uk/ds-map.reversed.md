---
navigation:
  - ds-map.reverse.md: '« Ds\\Map::reverse'
  - ds-map.skip.md: 'Ds\\Map::skip »'
  - index.md: PHP Manual
  - class.ds-map.md: Ds\\Map
title: 'Ds\\Map::reversed'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Map::reversed

(PECL ds >= 1.0.0)

Ds\\Map::reversed — Повертає перегорнуту копію колекції

### Опис

```methodsynopsis
public Ds\Map::reversed(): Ds\Map
```

Повертає копію колекції.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Перегорнута копія колекції.

> **Зауваження** :
> 
> Поточна колекція не зміниться.

### Приклади

**Приклад #1 Приклад використання** Ds\\Map::reversed()\*\*\*\*

```php
<?php
$map = new \Ds\Map(["a" => 1, "b" => 2, "c" => 3]);

print_r($map->reversed());
?>
```

Висновок наведеного прикладу буде схожим на:

```
Ds\Map Object
(
    [0] => Ds\Pair Object
        (
            [key] => c
            [value] => 3
        )

    [1] => Ds\Pair Object
        (
            [key] => b
            [value] => 2
        )

    [2] => Ds\Pair Object
        (
            [key] => a
            [value] => 1
        )

)
```

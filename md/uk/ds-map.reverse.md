---
navigation:
  - ds-map.remove.md: '« DsMap::remove'
  - ds-map.reversed.md: 'ДсMap::reversed »'
  - index.md: PHP Manual
  - class.ds-map.md: Коллекция пар ключ-значение
title: 'ДсMap::reverse'
---
# ДсMap::reverse

(PECL ds >= 1.0.0)

ДсMap::reverse — Перевертає поточну колекцію

### Опис

```methodsynopsis
public Ds\Map::reverse(): void
```

Перевертає поточну колекцію.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **ДсMap::reverse()****

```php
<?php
$map = new \Ds\Map(["a" => 1, "b" => 2, "c" => 3]);
$map->reverse();

print_r($map);
?>
```

Результатом виконання цього прикладу буде щось подібне:

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

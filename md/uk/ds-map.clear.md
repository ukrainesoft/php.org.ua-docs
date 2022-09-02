---
navigation:
  - ds-map.capacity.md: '« DsMap::capacity'
  - ds-map.construct.md: 'ДсMap::construct »'
  - index.md: PHP Manual
  - class.ds-map.md: Коллекция пар ключ-значение
title: 'ДсMap::clear'
---
# ДсMap::clear

(PECL ds >= 1.0.0)

ДсMap::clear — Видаляє всі значення з колекції

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

**Приклад #1 Приклад використання **ДсMap::clear()****

```php
<?php
$map = new \Ds\Map([
    "a" => 1,
    "b" => 2,
    "c" => 3,
]);
print_r($map);

$map->clear();
print_r($map);
?>
```

Результатом виконання цього прикладу буде щось подібне:

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

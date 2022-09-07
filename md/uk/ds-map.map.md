---
navigation:
  - ds-map.last.md: '« DsMap::last'
  - ds-map.merge.md: 'ДсMap::merge »'
  - index.md: PHP Manual
  - class.ds-map.md: Коллекция пар ключ-значение
title: 'ДсMap::map'
---
# ДсMap::map

(PECL ds >= 1.0.0)

ДсMap::map — Повертає результат застосування callback-функції до всіх значень колекції

### Опис

```methodsynopsis
public Ds\Map::map(callable $callback): Ds\Map
```

Повертає результат застосування callback-функції, переданої в `callback`до всіх значень колекції.

### Список параметрів

`callback`

```methodsynopsis
callback(mixed $key, mixed $value): mixed
```

Аргумент типу [callable](language.types.callable.md)

Ця функція повинна повертати нове значення для кожного елемента колекції.

### Значення, що повертаються

Результат застосування `callback` до кожного значення колекції.

> **Зауваження**
> 
> Значення поточної колекції залишаться незмінними.

### Приклади

**Приклад #1 Приклад використання **ДсMap::map()****

```php
<?php
$map = new \Ds\Map(["a" => 1, "b" => 2, "c" => 3]);

print_r($map->map(function($key, $value) { return $value * 2; }));
print_r($map);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
(
    [0] => Ds\Pair Object
        (
            [key] => a
            [value] => 2
        )

    [1] => Ds\Pair Object
        (
            [key] => b
            [value] => 4
        )

    [2] => Ds\Pair Object
        (
            [key] => c
            [value] => 6
        )

)
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

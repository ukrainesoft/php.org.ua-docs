---
navigation:
  - ds-map.last.md: '« Ds\\Map::last'
  - ds-map.merge.md: 'Ds\\Map::merge »'
  - index.md: PHP Manual
  - class.ds-map.md: Ds\\Map
title: 'Ds\\Map::map'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Map::map

(PECL ds >= 1.0.0)

Ds\\Map::map — Повертає результат застосування callback-функції до всіх значень колекції

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

Аргумент типа[callable](language.types.callable.md)

Ця функція повинна повертати нове значення для кожного елемента колекції.

### Значення, що повертаються

Результат применения`callback` до кожного значення колекції.

> **Зауваження** :
> 
> Значення поточної колекції залишаться незмінними.

### Приклади

**Пример #1 Пример использования**Ds\\Map::map()\*\*\*\*

```php
<?php
$map = new \Ds\Map(["a" => 1, "b" => 2, "c" => 3]);

print_r($map->map(function($key, $value) { return $value * 2; }));
print_r($map);
?>
```

Висновок наведеного прикладу буде схожим на:

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

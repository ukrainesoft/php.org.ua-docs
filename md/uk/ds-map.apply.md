---
navigation:
  - ds-map.allocate.html: '« DsMap::allocate'
  - ds-map.capacity.html: 'ДсMap::capacity »'
  - index.html: PHP Manual
  - class.ds-map.html: Коллекция пар ключ-значение
title: 'ДсMap::apply'
---
# ДсMap::apply

(PECL ds >= 1.0.0)

ДсMap::apply — Оновлення всіх значень застосуванням до них переданої callback-функції

### Опис

```methodsynopsis
public Ds\Map::apply(callable $callback): void
```

Оновлення всіх значень застосуванням до них переданої `callback`функції.

### Список параметрів

`callback`

```methodsynopsis
callback(mixed $key, mixed $value): mixed
```

Об'єкт типу [callable](language.types.callable.html)

Callback-функція має повертати нове значення, яке замінить поточне.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **ДсMap::apply()****

```php
<?php
$map = new \Ds\Map(["a" => 1, "b" => 2, "c" => 3]);
$map->apply(function($key, $value) { return $value * 2; });

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
```

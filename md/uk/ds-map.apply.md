---
navigation:
  - ds-map.allocate.md: '« Ds\\Map::allocate'
  - ds-map.capacity.md: 'Ds\\Map::capacity »'
  - index.md: PHP Manual
  - class.ds-map.md: Ds\\Map
title: 'Ds\\Map::apply'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Map::apply

(PECL ds >= 1.0.0)

Ds\\Map::apply — Оновлення всіх значень застосуванням до них переданої callback-функції

### Опис

```methodsynopsis
public Ds\Map::apply(callable $callback): void
```

Оновлення всіх значень застосуванням до них переданої `callback`\-функції.

### Список параметрів

`callback`

```methodsynopsis
callback(mixed $key, mixed $value): mixed
```

Об'єкт типу [callable](language.types.callable.md)

Callback-функція має повертати нове значення, яке замінить поточне.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Пример #1 Пример использования**Ds\\Map::apply()\*\*\*\*

```php
<?php
$map = new \Ds\Map(["a" => 1, "b" => 2, "c" => 3]);
$map->apply(function($key, $value) { return $value * 2; });

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

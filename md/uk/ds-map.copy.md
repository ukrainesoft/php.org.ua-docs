Повертає поверхневу копію колекції

-   [« DsMap::construct](ds-map.construct.html)
    
-   [ДсMap::count »](ds-map.count.html)
    
-   [PHP Manual](index.html)
    
-   [Коллекция пар ключ-значение](class.ds-map.html)
    
-   Повертає поверхневу копію колекції
    

# ДсMap::copy

(PECL ds >= 1.0.0)

ДсMap::copy — Повертає поверхневу копію колекції

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

**Приклад #1 Приклад використання **ДсMap::copy()****

```php
<?php
$map = new \Ds\Map([
    "a" => 1,
    "b" => 2,
    "c" => 3,
]);

print_r($map->copy());
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
```
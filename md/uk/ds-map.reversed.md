Повертає перегорнуту копію колекції

-   [« Ds\\Map::reverse](ds-map.reverse.html)
    
-   [Ds\\Map::skip »](ds-map.skip.html)
    
-   [PHP Manual](index.html)
    
-   [Коллекция пар ключ-значение](class.ds-map.html)
    
-   Повертає перегорнуту копію колекції
    

# ДсMap::reversed

(PECL ds >= 1.0.0)

ДсMap::reverse — Повертає перегорнуту копію колекції

### Опис

```methodsynopsis
public Ds\Map::reversed(): Ds\Map
```

Повертає копію колекції.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Перегорнута копія колекції.

> **Зауваження**
> 
> Поточна колекція не зміниться.

### Приклади

**Приклад #1 Приклад використання **ДсMap::reversed()****

```php
<?php
$map = new \Ds\Map(["a" => 1, "b" => 2, "c" => 3]);

print_r($map->reversed());
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
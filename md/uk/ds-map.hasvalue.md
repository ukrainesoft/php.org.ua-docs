Перевіряє, чи колекція містить задане значення

-   [« DsMap::hasKey](ds-map.haskey.html)
    
-   [ДсMap::intersect »](ds-map.intersect.html)
    
-   [PHP Manual](index.html)
    
-   [Коллекция пар ключ-значение](class.ds-map.html)
    
-   Перевіряє, чи колекція містить задане значення
    

# ДсMap::hasValue

(PECL ds >= 1.0.0)

ДсMap::hasValue — Перевіряє, чи колекція містить задане значення

### Опис

```methodsynopsis
public Ds\Map::hasValue(mixed $value): bool
```

Перевіряє, чи колекція містить задане значення.

### Список параметрів

`value`

Значення для перевірки.

### Значення, що повертаються

Повертає \*\*`true`\*\*якщо ключ знайдений, інакше **`false`**

### Приклади

**Приклад #1 Приклад використання **ДсMap::hasValue()****

```php
<?php
$map = new \Ds\Map(["a" => 1, "b" => 2, "c" => 3]);

var_dump($map->hasValue(1)); // true
var_dump($map->hasValue(4)); // false
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
bool(true)
bool(false)
```
Повертає поточну місткість

-   [« DsMap::apply](ds-map.apply.html)
    
-   [ДсMap::clear »](ds-map.clear.html)
    
-   [PHP Manual](index.html)
    
-   [Коллекция пар ключ-значение](class.ds-map.html)
    
-   Повертає поточну місткість
    

# ДсMap::capacity

(PECL ds >= 1.0.0)

ДсMap::capacity — Повертає поточну місткість

### Опис

```methodsynopsis
public Ds\Map::capacity(): int
```

Повертає поточну місткість.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Поточна місткість.

### Приклади

**Приклад #1 Приклад використання **ДсMap::capacity()****

```php
<?php
$map = new \Ds\Map();
var_dump($map->capacity());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
int(16)
```
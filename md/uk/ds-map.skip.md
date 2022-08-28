Повертає пару за індексом позиції

-   [« Ds\\Map::reversed](ds-map.reversed.html)
    
-   [Ds\\Map::slice »](ds-map.slice.html)
    
-   [PHP Manual](index.html)
    
-   [Коллекция пар ключ-значение](class.ds-map.html)
    
-   Повертає пару за індексом позиції
    

# ДсMap::skip

(PECL ds >= 1.0.0)

ДсMap::skip — Повертає пару за індексом позиції

### Опис

```methodsynopsis
public Ds\Map::skip(int $position): Ds\Pair
```

Повертає пару за індексом позиції `position`, перша пара має індекс 0

### Список параметрів

`position`

Індекс позиції.

### Значення, що повертаються

Повертає **ДсPair** із заданої позиції `position`

### Помилки

Викидає виняток [OutOfRangeException](class.outofrangeexception.html)якщо індекс некоректний.

### Приклади

**Приклад #1 Приклад використання **ДсMap::skip()****

```php
<?php
$map = new \Ds\Map(["a" => 1, "b" => 2, "c" => 3]);

var_dump($map->skip(1));
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
object(Ds\Pair)#2 (2) {
  ["key"]=>
  string(1) "b"
  ["value"]=>
  int(2)
}
```
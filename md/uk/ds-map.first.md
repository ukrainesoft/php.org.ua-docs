Повертає перший елемент колекції

-   [« Ds\\Map::filter](ds-map.filter.html)
    
-   [Ds\\Map::get »](ds-map.get.html)
    
-   [PHP Manual](index.html)
    
-   [Коллекция пар ключ-значение](class.ds-map.html)
    
-   Повертає перший елемент колекції
    

# ДсMap::first

(PECL ds >= 1.0.0)

ДсMap::first — Повертає перший елемент колекції

### Опис

```methodsynopsis
public Ds\Map::first(): Ds\Pair
```

Повертає перший елемент колекції.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Перший елемент колекції.

### Помилки

Викидає виняток [UnderflowException](class.underflowexception.html)якщо колекція порожня.

### Приклади

**Приклад #1 Приклад використання **ДсMap::first()****

```php
<?php
$map = new \Ds\Map(["a" => 1, "b" => 2, "c" => 3]);
var_dump($map->first());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
object(Ds\Pair)#2 (2) {
  ["key"]=>
  string(1) "a"
  ["value"]=>
  int(1)
}
```
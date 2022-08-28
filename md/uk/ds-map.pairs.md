Повертає послідовність, що містить усі пари колекції

-   [« Ds\\Map::merge](ds-map.merge.html)
    
-   [Ds\\Map::put »](ds-map.put.html)
    
-   [PHP Manual](index.html)
    
-   [Коллекция пар ключ-значение](class.ds-map.html)
    
-   Повертає послідовність, що містить усі пари колекції
    

# ДсMap::pairs

(PECL ds >= 1.0.0)

ДсMap::pairs — Повертає послідовність, яка містить усі пари колекції.

### Опис

```methodsynopsis
public Ds\Map::pairs(): Ds\Sequence
```

Повертає **ДсSequence**, що містить усі пари колекції.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

**ДсSequence**, що містить усі пари вихідної колекції.

### Приклади

**Приклад #1 Приклад використання **ДсMap::pairs()****

```php
<?php
$map = new \Ds\Map(["a" => 1, "b" => 2, "c" => 3]);

var_dump($map->pairs());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
object(Ds\Map)#8 (3) {
  [0]=>
  object(Ds\Pair)#5 (2) {
    ["key"]=>
    string(1) "a"
    ["value"]=>
    int(1)
  }
  [1]=>
  object(Ds\Pair)#6 (2) {
    ["key"]=>
    string(1) "b"
    ["value"]=>
    int(2)
  }
  [2]=>
  object(Ds\Pair)#7 (2) {
    ["key"]=>
    string(1) "c"
    ["value"]=>
    int(3)
  }
}
p
```
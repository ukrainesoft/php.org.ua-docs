Створює нову колекцію пар із елементів, вибраних за допомогою заданої callback-функції

-   [« DsMap::diff](ds-map.diff.html)
    
-   [ДсMap::first »](ds-map.first.html)
    
-   [PHP Manual](index.html)
    
-   [Коллекция пар ключ-значение](class.ds-map.html)
    
-   Створює нову колекцію пар із елементів, вибраних за допомогою заданої callback-функції
    

# ДсMap::filter

(PECL ds >= 1.0.0)

ДсMap::filter — Створює нову колекцію пар із елементів, вибраних за допомогою заданої callback-функції

### Опис

```methodsynopsis
public Ds\Map::filter(callable $callback = ?): Ds\Map
```

Створює нову колекцію пар із елементів, вибраних за допомогою заданої callback-функції.

### Список параметрів

`callback`

```methodsynopsis
callback(mixed $key, mixed $value): bool
```

Опціональний аргумент типу [callable](language.types.callable.html), який повертає **`true`**, якщо пара повинна бути включена та **`false`**, якщо ні.

Якщо callback-функція не задана, будуть включені тільки елементи, які призводять до логічного значення **`true`** (дивіться розділ з [приведением к boolean](language.types.boolean.html#language.types.boolean.casting)

### Значення, що повертаються

Нова колекція пар, що містить значення, для яких `callback`функція повернула **`true`**, або всі елементи, які при приведенні до логічного типу стають **`true`**, якщо параметр `callback` не заданий.

### Приклади

**Приклад #1 Приклад **ДсMap::filter()** з використанням callback-функції**

```php
<?php
$map = new \Ds\Map(["a", "b", "c", "d", "e"]);

var_dump($map->filter(function($key, $value) {
    return $key % 2 == 0;
}));
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
object(Ds\Map)#3 (3) {
  [0]=>
  object(Ds\Pair)#2 (2) {
    ["key"]=>
    int(0)
    ["value"]=>
    string(1) "a"
  }
  [1]=>
  object(Ds\Pair)#4 (2) {
    ["key"]=>
    int(2)
    ["value"]=>
    string(1) "c"
  }
  [2]=>
  object(Ds\Pair)#5 (2) {
    ["key"]=>
    int(4)
    ["value"]=>
    string(1) "e"
  }
}
```

**Приклад #2 Приклад **ДсMap::filter()** без callback-функції**

```php
<?php
$map = new \Ds\Map(["a" => 0, "b" => 1, "c" => true, "d" => false]);

var_dump($map->filter());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
object(Ds\Map)#2 (3) {
  [0]=>
  int(1)
  [1]=>
  string(1) "a"
  [2]=>
  bool(true)
}
```
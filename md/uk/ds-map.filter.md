---
navigation:
  - ds-map.diff.md: '« Ds\\Map::diff'
  - ds-map.first.md: 'Ds\\Map::first »'
  - index.md: PHP Manual
  - class.ds-map.md: Ds\\Map
title: 'Ds\\Map::filter'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Map::filter

(PECL ds >= 1.0.0)

Ds\\Map::filter — Створює нову колекцію пар із елементів, вибраних за допомогою заданої callback-функції

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

Опціональний аргумент типу [callable](language.types.callable.md), який повертає **`true`**, якщо пара повинна бути включена та **`false`**, якщо ні.

Якщо callback-функція не задана, будуть включені тільки елементи, які призводять до логічного значення **`true`**(смотрите раздел с[приведенням до boolean](language.types.boolean.md#language.types.boolean.casting)

### Значення, що повертаються

Нова колекція пар, що містить значення, для яких `callback`\-функція повернула **`true`**, або всі елементи, які при приведенні до логічного типу стають **`true`**, якщо параметр `callback`не задан.

### Приклади

**Пример #1 Пример**Ds\\Map::filter()**с использованием callback-функции**

```php
<?php
$map = new \Ds\Map(["a", "b", "c", "d", "e"]);

var_dump($map->filter(function($key, $value) {
    return $key % 2 == 0;
}));
?>
```

Висновок наведеного прикладу буде схожим на:

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

**Пример #2 Пример**Ds\\Map::filter()\*\* без callback-функції\*\*

```php
<?php
$map = new \Ds\Map(["a" => 0, "b" => 1, "c" => true, "d" => false]);

var_dump($map->filter());
?>
```

Висновок наведеного прикладу буде схожим на:

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

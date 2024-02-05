---
navigation:
  - ds-map.count.md: '« Ds\\Map::count'
  - ds-map.filter.md: 'Ds\\Map::filter »'
  - index.md: PHP Manual
  - class.ds-map.md: Ds\\Map
title: 'Ds\\Map::diff'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Map::diff

(PECL ds >= 1.0.0)

Ds\\Map::diff — Створює нову колекцію пар з елементами, ключів яких немає в іншій колекції пар

### Опис

```methodsynopsis
public Ds\Map::diff(Ds\Map $map): Ds\Map
```

Повертає нову колекцію пар, що не містить елементів із ключами, які присутні в колекції пар, переданої в `map`

`A \ B = {x ∈ A | x ∉ B}`

### Список параметрів

`map`

Колекція пар містить елементи з ключами, яких не повинно бути в новій колекції пар.

### Значення, що повертаються

Результат видалення всіх елементів, ключі яких є в колекції пар, переданої в `map`

### Дивіться також

-   [» Різниця масивів](https://en.wikipedia.org/wiki/Complement_(set_theory))на Wikipedia

### Приклади

**Пример #1 Пример использования**Ds\\Map::diff()\*\*\*\*

```php
<?php
$a = new \Ds\Map(["a" => 1, "b" => 2, "c" => 3]);
$b = new \Ds\Map(["b" => 4, "c" => 5, "d" => 6]);

var_dump($a->diff($b));
?>
```

Висновок наведеного прикладу буде схожим на:

```
object(Ds\Map)#3 (1) {
  [0]=>
  object(Ds\Pair)#4 (2) {
    ["key"]=>
    string(1) "a"
    ["value"]=>
    int(1)
  }
}
```

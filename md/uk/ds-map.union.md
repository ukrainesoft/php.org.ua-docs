---
navigation:
  - ds-map.toarray.md: '« Ds\\Map::toArray'
  - ds-map.values.md: 'Ds\\Map::values »'
  - index.md: PHP Manual
  - class.ds-map.md: Ds\\Map
title: 'Ds\\Map::union'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Map::union

(PECL ds >= 1.0.0)

Ds\\Map::union — Створює нову колекцію пар із елементів двох колекцій

### Опис

```methodsynopsis
public Ds\Map::union(Ds\Map $map): Ds\Map
```

Створює нову колекцію пар, що містить пари поточної та переданої в `map` колекцій.

`A ∪ B = {x: x ∈ A ∨ x ∈ B}`

> **Зауваження** :
> 
> У разі збігу ключів значення елементів будуть братися з переданої колекції.

### Список параметрів

`map`

Нова колекція для об'єднання з поточною.

### Значення, що повертаються

Нова колекція пар, що є об'єднанням поточної та переданої в `map`

### Дивіться також

-   [» Об'єднання](https://en.wikipedia.org/wiki/Union_(set_theory))в Вікіпедія

### Приклади

**Приклад #1 Приклад використання** Ds\\Map::union()\*\*\*\*

```php
<?php
$a = new \Ds\Map(["a" => 1, "b" => 2, "c" => 3]);
$b = new \Ds\Map(["b" => 3, "c" => 4, "d" => 5]);

print_r($a->union($b));
?>
```

Висновок наведеного прикладу буде схожим на:

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
            [value] => 3
        )

    [2] => Ds\Pair Object
        (
            [key] => c
            [value] => 4
        )

    [3] => Ds\Pair Object
        (
            [key] => d
            [value] => 5
        )

)
```

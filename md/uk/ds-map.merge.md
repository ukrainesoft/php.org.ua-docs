---
navigation:
  - ds-map.map.md: '« Ds\\Map::map'
  - ds-map.pairs.md: 'Ds\\Map::pairs »'
  - index.md: PHP Manual
  - class.ds-map.md: Ds\\Map
title: 'Ds\\Map::merge'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Map::merge

(PECL ds >= 1.0.0)

Ds\\Map::merge — Повертає результат додавання всіх заданих елементів до колекції

### Опис

```methodsynopsis
public Ds\Map::merge(mixed $values): Ds\Map
```

Повертає результат додавання всіх ключів переданого об'єкта класу [traversable](class.traversable.md) або масиву (array) з відповідними значеннями поточної колекції.

> **Зауваження** :
> 
> Значення поточної колекції буде перезаписано, якщо передані ключі вже існують.

### Список параметрів

`values`

Об'єкт класу [traversable](class.traversable.md)или array.

### Значення, що повертаються

Повертає результат додавання всіх ключів переданого об'єкта класу [traversable](class.traversable.md) або масиву з відповідними значеннями до поточної колекції

> **Зауваження** :
> 
> Поточний екземпляр колекції залишиться недоторканим.

### Приклади

**Пример #1 Пример использования**Ds\\Map::merge()\*\*\*\*

```php
<?php
$map = new \Ds\Map(["a" => 1, "b" => 2, "c" => 3]);

print_r($map->merge(["a" => 10, "e" => 50]));
?>
```

Висновок наведеного прикладу буде схожим на:

```
Ds\Map Object
(
    [0] => Ds\Pair Object
        (
            [key] => a
            [value] => 10
        )

    [1] => Ds\Pair Object
        (
            [key] => b
            [value] => 2
        )

    [2] => Ds\Pair Object
        (
            [key] => c
            [value] => 3
        )

    [3] => Ds\Pair Object
        (
            [key] => e
            [value] => 50
        )

)
```

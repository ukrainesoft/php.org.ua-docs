- [«Ds\Map::map](ds-map.map.md)
- [Ds\Map::pairs »](ds-map.pairs.md)

- [PHP Manual](index.md)
- [Колекція пар ключ-значення](class.ds-map.md)
- Повертає результат додавання всіх заданих елементів до колекції

# Ds\Map::merge

(PECL ds \>= 1.0.0)

Ds\Map::merge — Повертає результат додавання всіх заданих елементів
у колекцію

### Опис

public
**Ds\Map::merge**([mixed](language.types.declarations.md#language.types.declarations.mixed)
`$values`): [Ds\Map](class.ds-map.md)

Повертає результат додавання всіх ключів переданого об'єкту класу
[traversable](class.traversable.md) або масиву (array) з
відповідними значеннями у поточну колекцію.

> **Примітка**:
>
> Значення поточної колекції буде перезаписано, якщо передані ключі
> вже є.

### Список параметрів

`values`
Об'єкт класу [traversable](class.traversable.md) або array.

### Значення, що повертаються

Повертає результат додавання всіх ключів переданого об'єкту класу
[traversable](class.traversable.md) або масиву з відповідними
значеннями у поточну колекцію

> **Примітка**:
>
> Поточний екземпляр колекції залишиться недоторканим.

### Приклади

**Приклад #1 Приклад використання **Ds\Map::merge()****

` <?php$map = new \Ds\Map(["a" => 1, "b" => 2, c" => 3]);print_r($map->merge(["a" = > 10, "e" => 50]));?> `

Результатом виконання цього прикладу буде щось подібне:

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

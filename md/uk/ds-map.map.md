- [« Ds\Map::last](ds-map.last.md)
- [Ds\Map::merge »](ds-map.merge.md)

- [PHP Manual](index.md)
- [Колекція пар ключ-значення](class.ds-map.md)
- Повертає результат застосування callback-функції до всіх значень
колекції

# Ds\Map::map

(PECL ds \>= 1.0.0)

Ds\Map::map — Повертає результат застосування callback-функції до всіх
значенням колекції

### Опис

public **Ds\Map::map**([callable](language.types.callable.md)
`$callback`): [Ds\Map](class.ds-map.md)

Повертає результат застосування callback-функції, переданої в
`callback`, до всіх значень колекції.

### Список параметрів

`callback`
callback([mixed](language.types.declarations.md#language.types.declarations.mixed)
`$key`,
[mixed](language.types.declarations.md#language.types.declarations.mixed)
`$value`):
[mixed](language.types.declarations.md#language.types.declarations.mixed)

Аргумент типу [callable](language.types.callable.md).

Ця функція повинна повертати нове значення для кожного елемента
колекції.

### Значення, що повертаються

Результат застосування `callback` до кожного значення колекції.

> **Примітка**:
>
> Значення поточної колекції залишаться незмінними.

### Приклади

**Приклад #1 Приклад використання **Ds\Map::map()****

` <?php$map = new \Ds\Map(["a" => 1, "b" => 2, c" => 3]);print_r($map->map(function($key, $value) { return $value * 2; }));print_r($map);?> `

Результатом виконання цього прикладу буде щось подібне:

(
[0] => Ds\Pair Object
(
[key] => a
[value] => 2
)

[1] => Ds\Pair Object
(
[key] => b
[value] => 4
)

[2] => Ds\Pair Object
(
[key] => c
[value] => 6
)

)
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
[value] => 2
)

[2] => Ds\Pair Object
(
[key] => c
[value] => 3
)

)

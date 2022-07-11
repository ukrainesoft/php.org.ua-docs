- [« Ds\Map::allocate](ds-map.allocate.md)
- [Ds\Map::capacity »](ds-map.capacity.md)

- [PHP Manual](index.md)
- [Колекція пар ключ-значення](class.ds-map.md)
- Оновлення всіх значень застосуванням до них переданої
callback-функції

# Ds\Map::apply

(PECL ds \>= 1.0.0)

Ds\Map::apply — Оновлення всіх значень застосуванням до них переданої
callback-функції

### Опис

public **Ds\Map::apply**([callable](language.types.callable.md)
`$callback`): void

Оновлення всіх значень застосуванням до них переданої
'callback'-функції.

### Список параметрів

`callback`
callback([mixed](language.types.declarations.md#language.types.declarations.mixed)
`$key`,
[mixed](language.types.declarations.md#language.types.declarations.mixed)
`$value`):
[mixed](language.types.declarations.md#language.types.declarations.mixed)

Об'єкт типу [callable](language.types.callable.md).

Callback-функція має повертати нове значення, яке замінить
поточний.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **Ds\Map::apply()****

` <?php$map = new \Ds\Map(["a" => 1, "b" => 2, c" => 3]);$map->apply(function($key, $value) ) { return $value * 2; });print_r($map);?> `

Результатом виконання цього прикладу буде щось подібне:

Ds\Map Object
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

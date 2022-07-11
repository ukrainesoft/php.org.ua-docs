- [« Ds\Map::capacity](ds-map.capacity.md)
- [Ds\Map::\_\_construct »](ds-map.construct.md)

- [PHP Manual](index.md)
- [Колекція пар ключ-значення](class.ds-map.md)
- Видаляє всі значення з колекції

# Ds\Map::clear

(PECL ds \>= 1.0.0)

Ds\Map::clear — Видаляє всі значення колекції.

### Опис

public **Ds\Map::clear**(): void

Видаляє всі значення колекції.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **Ds\Map::clear()****

` <?php$map = new \Ds\Map([   "a" => 1,   "b" => 2,    "c" => 3,]);print_r($map);$map->ar );print_r($map);?> `

Результатом виконання цього прикладу буде щось подібне:

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
Ds\Map Object
(
)

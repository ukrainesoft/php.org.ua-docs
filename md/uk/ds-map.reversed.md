- [« Ds\Map::reverse](ds-map.reverse.md)
- [Ds\Map::skip »](ds-map.skip.md)

- [PHP Manual](index.md)
- [Колекція пар ключ-значення](class.ds-map.md)
- Повертає перегорнуту копію колекції

# Ds\Map::reversed

(PECL ds \>= 1.0.0)

Ds\Map::reversed — Повертає перегорнуту копію колекції

### Опис

public **Ds\Map::reversed**(): [Ds\Map](class.ds-map.md)

Повертає копію колекції.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Перегорнута копія колекції.

> **Примітка**:
>
> Поточна колекція не зміниться.

### Приклади

**Приклад #1 Приклад використання **Ds\Map::reversed()****

` <?php$map = new \Ds\Map(["a" => 1, "b" => 2, c" => 3]);print_r($map->reversed());?> `

Результатом виконання цього прикладу буде щось подібне:

Ds\Map Object
(
[0] => Ds\Pair Object
(
[key] => c
[value] => 3
)

[1] => Ds\Pair Object
(
[key] => b
[value] => 2
)

[2] => Ds\Pair Object
(
[key] => a
[value] => 1
)

)

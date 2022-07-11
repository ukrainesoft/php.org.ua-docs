- [« Ds\Map::toArray](ds-map.toarray.md)
- [Ds\Map::values »](ds-map.values.md)

- [PHP Manual](index.md)
- [Колекція пар ключ-значення](class.ds-map.md)
- Створює нову колекцію пар із елементів двох колекцій

# Ds\Map::union

(PECL ds \>= 1.0.0)

Ds\Map::union — Створює нову колекцію пар із елементів двох колекцій

### Опис

public **Ds\Map::union**([Ds\Map](class.ds-map.md) `$map`):
[Ds\Map](class.ds-map.md)

Створює нову колекцію пар, що містить пари поточної та переданої в
`map` колекцій.

`A ∪ B = {x: x ∈ A ∨ x ∈ B}`

> **Примітка**:
>
> У разі збігу ключів значення елементів будуть братися з
> переданої колекції.

### Список параметрів

`map`
Нова колекція для об'єднання з поточною.

### Значення, що повертаються

Нова колекція пар, що є об'єднанням поточної та переданої в
`map`.

### Також дивіться

- [» Об'єднання](https://en.wikipedia.org/wiki/Union_(set_theory)) в
Вікіпедія

### Приклади

**Приклад #1 Приклад використання **Ds\Map::union()****

` <?php$a = new \Ds\Map(["a" => 1, "b" => 2, c" => 3]);$b = new \Ds\Map(["b" => 3, "c" => 4, "d" => 5]);print_r($a->union($b));?> `

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

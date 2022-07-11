- [« Ds\Map::jsonSerialize](ds-map.jsonserialize.md)
- [Ds\Map::ksort »](ds-map.ksort.md)

- [PHP Manual](index.md)
- [Колекція пар ключ-значення](class.ds-map.md)
- Повертає набір ключів колекції

# Ds\Map::keys

(PECL ds \>= 1.0.0)

Ds\Map::keys — Повертає набір ключів колекції

### Опис

public **Ds\Map::keys**(): [Ds\Set](class.ds-set.md)

Повертає набір ключів колекції із збереженням їх порядку.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Колекція **Ds\Set**, яка містить усі ключі поточної колекції.

### Приклади

**Приклад #1 Приклад використання **Ds\Map::keys()****

` <?php$map = new \Ds\Map(["a" => 1, "b" => 2, c" => 3]);var_dump($map->keys());?> `

Результатом виконання цього прикладу буде щось подібне:

object(Ds\Set)#2 (3) {
[0]=>
string(1) "a"
[1]=>
string(1) "b"
[2]=>
string(1) "c"
}

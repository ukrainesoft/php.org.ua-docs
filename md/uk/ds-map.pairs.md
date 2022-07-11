- [«Ds\Map::merge](ds-map.merge.md)
- [Ds\Map::put »](ds-map.put.md)

- [PHP Manual](index.md)
- [Колекція пар ключ-значення](class.ds-map.md)
- Повертає послідовність, що містить усі пари колекції

# Ds\Map::pairs

(PECL ds \>= 1.0.0)

Ds\Map::pairs — Повертає послідовність, яка містить усі пари
колекції

### Опис

public **Ds\Map::pairs**(): [Ds\Sequence](class.ds-sequence.md)

Повертає **Ds\Sequence**, що містить усі пари колекції.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

**Ds\Sequence**, що містить усі пари вихідної колекції.

### Приклади

**Приклад #1 Приклад використання **Ds\Map::pairs()****

` <?php$map = new \Ds\Map(["a" => 1, "b" => 2, c" => 3]);var_dump($map->pairs());?> `

Результатом виконання цього прикладу буде щось подібне:

object(Ds\Map)#8 (3) {
[0]=>
object(Ds\Pair)#5 (2) {
["key"]=>
string(1) "a"
["value"]=>
int(1)
}
[1]=>
object(Ds\Pair)#6 (2) {
["key"]=>
string(1) "b"
["value"]=>
int(2)
}
[2]=>
object(Ds\Pair)#7 (2) {
["key"]=>
string(1) "c"
["value"]=>
int(3)
}
}
p

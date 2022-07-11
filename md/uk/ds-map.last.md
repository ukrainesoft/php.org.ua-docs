- [« Ds\Map::ksorted](ds-map.ksorted.md)
- [Ds\Map::map »](ds-map.map.md)

- [PHP Manual](index.md)
- [Колекція пар ключ-значення](class.ds-map.md)
- Повертає останню пару колекції

# Ds\Map::last

(PECL ds \>= 1.0.0)

Ds\Map::last — Повертає останню пару колекції

### Опис

public **Ds\Map::last**(): [Ds\Pair](class.ds-pair.md)

Повертає останню пару колекції.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Останній елемент колекції.

### Помилки

Викидає виняток
[UnderflowException](class.underflowexception.md), якщо колекція
порожня.

### Приклади

**Приклад #1 Приклад використання **Ds\Map::last()****

` <?php$map = new \Ds\Map(["a" => 1, "b" => 2, "c" => 3]);var_dump($map->last());?> `

Результатом виконання цього прикладу буде щось подібне:

object(Ds\Pair)#2 (2) {
["key"]=>
string(1) "c"
["value"]=>
int(3)
}

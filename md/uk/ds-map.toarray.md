- [«Ds\Map::sum](ds-map.sum.md)
- [Ds\Map::union »](ds-map.union.md)

- [PHP Manual](index.md)
- [Колекція пар ключ-значення](class.ds-map.md)
- Перетворює колекцію на array

# Ds\Map::toArray

(PECL ds \>= 1.0.0)

Ds\Map::toArray — Перетворює колекцію на array

### Опис

public **Ds\Map::toArray**(): array

Перетворює колекцію на array.

**Застереження**

Колекції пар, що містять нескалярні ключі, не можуть бути перетворені
масив (array).

**Застереження**

Масив (array) вважатиме всі числові ключі за цілі, тобто.
обидва ключі ``1'` і `1` будуть сприйняті як `1` і тільки один з
елементів потрапить у результуючий масив

> **Примітка**:
>
> Приведення до типу array поки що не підтримується.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Масив (array), що містить всі елементи колекції із збереженням їх
порядку.

### Приклади

**Приклад #1 Приклад використання **Ds\Map::toArray()****

` <?php$map = new \Ds\Map([   "a" => 1,   "b" => 2,   "c" => 3,]);var_dump($map->toArray() > `

Результатом виконання цього прикладу буде щось подібне:

array(3) {
["a"]=>
int(1)
["b"]=>
int(2)
["c"]=>
int(3)
}

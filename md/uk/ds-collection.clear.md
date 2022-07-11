- [«Колекція](class.ds-collection.md)
- [Ds\Collection::copy »](ds-collection.copy.md)

- [PHP Manual](index.md)
- [Колекція](class.ds-collection.md)
- Видаляє всі значення

# Ds\Collection::clear

(PECL ds \>= 1.0.0)

Ds\Collection::clear — Видаляє всі значення

### Опис

abstract public **Ds\Collection::clear**(): void

Видаляє всі значення колекції.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад **Ds\Collection::clear()****

` <?php$collection = new \Ds\Vector([1, 2, 3]);print_r($collection);$collection->clear();print_r($collection);?> `

Результатом виконання цього прикладу буде щось подібне:

Ds\Vector Object
(
[0] => 1
[1] => 2
[2] => 3
)
Ds\Vector Object
(
)

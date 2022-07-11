- [Ds\Set::capacity](ds-set.capacity.md)
- [Ds\Set::\_\_construct »](ds-set.construct.md)

- [PHP Manual](index.md)
- [Набір](class.ds-set.md)
- Видаляє всі значення з колекції

# Ds\Set::clear

(PECL ds \>= 1.0.0)

Ds\Set::clear — Видаляє всі значення колекції.

### Опис

public **Ds\Set::clear**(): void

Видаляє всі значення колекції.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **Ds\Set::clear()****

` <?php$set = new \Ds\Set([1, 2, 3]);print_r($set);$set->clear();print_r($set);?> `

Результатом виконання цього прикладу буде щось подібне:

Ds\Set Object
(
[0] => 1
[1] => 2
[2] => 3
)
Ds\Set Object
(
)

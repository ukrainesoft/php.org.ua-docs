- [« Ds\Stack::clear](ds-stack.clear.md)
- [Ds\Stack::copy »](ds-stack.copy.md)

- [PHP Manual](index.md)
- [Стек](class.ds-stack.md)
- Створює новий екземпляр класу

# Ds\Stack::\_\_construct

(PECL ds \>= 1.0.0)

Ds\Stack::\_\_construct — Створює новий екземпляр класу

### Опис

public
**Ds\Stack::\_\_construct**([mixed](language.types.declarations.md#language.types.declarations.mixed)
$values = ?)

Створює новий екземпляр класу, використовуючи або об'єкт реалізує
[traversable](class.traversable.md), або масив, передані в
як параметр `values`.

### Список параметрів

`values`
Об'єкт, що реалізує інтерфейс traversable або масив.

### Приклади

**Приклад #1 Приклад використання **Ds\Stack::\_\_construct()****

` <?php$stack = new \Ds\Stack();print_r($stack);$stack = new \Ds\Stack([1, 2, 3]);print_r($stack);?> `

Результатом виконання цього прикладу буде щось подібне:

Ds\Stack Object
(
)
Ds\Stack Object
(
[0] => 3
[1] => 2
[2] => 1
)

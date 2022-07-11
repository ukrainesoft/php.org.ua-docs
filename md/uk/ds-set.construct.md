- [« Ds\Set::clear](ds-set.clear.md)
- [Ds\Set::contains »](ds-set.contains.md)

- [PHP Manual](index.md)
- [Набір](class.ds-set.md)
- Створює новий екземпляр класу

# Ds\Set::\_\_construct

(PECL ds \>= 1.0.0)

Ds\Set::\_\_construct — Створює новий екземпляр класу

### Опис

public
**Ds\Set::\_\_construct**([mixed](language.types.declarations.md#language.types.declarations.mixed)
`$values` = [])

Створює новий екземпляр класу, використовуючи або об'єкт, що реалізує [traversable](class.traversable.md), або масив, передані в
як параметр `values`.

### Список параметрів

`values`
Об'єкт, що реалізує інтерфейс traversable або масив.

### Приклади

**Приклад #1 Приклад використання **Ds\Set::\_\_construct()****

` <?php$set = new \Ds\Set();var_dump($set);$set = new \Ds\Set([1, 2, 3]);var_dump($set);?> `

Результатом виконання цього прикладу буде щось подібне:

object(Ds\Set)#1 (0) {
}
object(Ds\Set)#2 (3) {
[0]=>
int(1)
[1]=>
int(2)
[2]=>
int(3)
}

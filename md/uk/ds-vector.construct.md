- [« Ds\Vector::clear](ds-vector.clear.md)
- [Ds\Vector::contains »](ds-vector.contains.md)

- [PHP Manual](index.md)
- [Вектор](class.ds-vector.md)
- Створює новий екземпляр

# Ds\Vector::\_\_construct

(PECL ds \>= 1.0.0)

Ds\Vector::\_\_construct — Створює новий екземпляр

### Опис

public
**Ds\Vector::\_\_construct**([mixed](language.types.declarations.md#language.types.declarations.mixed)
$values = ?)

Створює новий екземпляр, використовуючи або об'єкт реалізує
[traversable](class.traversable.md), або масив, передані в
як параметр `values`.

### Список параметрів

`values`
Об'єкт, що реалізує інтерфейс traversable або масив.

### Приклади

**Приклад #1 Приклад використання **Ds\Vector::\_\_construct()****

` <?php$vector = new \Ds\Vector();var_dump($vector);$vector = new \Ds\Vector([1, 2, 3]);var_dump($vector);?> `

Результатом виконання цього прикладу буде щось подібне:

object(Ds\Vector)#2 (0) {
}
object(Ds\Vector)#2 (3) {
[0]=>
int(1)
[1]=>
int(2)
[2]=>
int(3)
}

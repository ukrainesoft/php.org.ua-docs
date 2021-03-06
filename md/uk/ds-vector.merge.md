- [« Ds\Vector::map](ds-vector.map.md)
- [Ds\Vector::pop »](ds-vector.pop.md)

- [PHP Manual](index.md)
- [Вектор](class.ds-vector.md)
- Повертає результат додавання всіх заданих значень у вектор

# Ds\Vector::merge

(PECL ds \>= 1.0.0)

Ds\Vector::merge — Повертає результат додавання всіх даних
значень у вектор

### Опис

public
**Ds\Vector::merge**([mixed](language.types.declarations.md#language.types.declarations.mixed)
`$values`): [Ds\Vector](class.ds-vector.md)

Повертає результат додавання всіх заданих значень вектор.

### Список параметрів

`values`
Об'єкт класу [traversable](class.traversable.md) чи масив (array).

### Значення, що повертаються

Результат додавання всіх переданих значень вектор. Фактично
робиться копія вектора, який додаються значення.

> **Примітка**:
>
> Поточний екземпляр вектора залишиться недоторканим.

### Приклади

**Приклад #1 Приклад використання **Ds\Vector::merge()****

` <?php$vector = new \Ds\Vector([1, 2, 3]);var_dump($vector->merge([4, 5, 6]));var_dump($vector);?> `

Результатом виконання цього прикладу буде щось подібне:

object(Ds\Vector)#2 (6) {
[0]=>
int(1)
[1]=>
int(2)
[2]=>
int(3)
[3]=>
int(4)
[4]=>
int(5)
[5]=>
int(6)
}
object(Ds\Vector)#1 (3) {
[0]=>
int(1)
[1]=>
int(2)
[2]=>
int(3)
}

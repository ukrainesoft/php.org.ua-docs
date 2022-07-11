- [« Ds\Vector::rotate](ds-vector.rotate.md)
- [Ds\Vector::shift »](ds-vector.shift.md)

- [PHP Manual](index.md)
- [Вектор](class.ds-vector.md)
- Замінює значення за вказаним індексом

# Ds\Vector::set

(PECL ds \>= 1.0.0)

Ds\Vector::set — Замінює значення за вказаним індексом

### Опис

public **Ds\Vector::set**(int `$index`,
[mixed](language.types.declarations.md#language.types.declarations.mixed)
`$value`): void

Замінює значення за вказаним індексом.

### Список параметрів

`index`
Індекс, яким треба замінити значення.

`value`
Нове значення.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

Викидає виняток
[OutOfRangeException](class.outofrangeexception.md), якщо індекс
некоректний.

### Приклади

**Приклад #1 Приклад використання **Ds\Vector::set()****

` <?php$vector = new \Ds\Vector(["a", "b", "c"]);$vector->set(1, "_");print_r($vector);?> `

Результатом виконання цього прикладу буде щось подібне:

Ds\Vector Object
(
[0] => a
[1] => _
[2] => c
)

**Приклад #2 Приклад використання **Ds\Vector::set()** із синтаксисом
масиву**

` <?php$vector = new \Ds\Vector(["a", "b", "c"]);$vector[1] = "_";print_r($vector);?> `

Результатом виконання цього прикладу буде щось подібне:

Ds\Vector Object
(
[0] => a
[1] => _
[2] => c
)

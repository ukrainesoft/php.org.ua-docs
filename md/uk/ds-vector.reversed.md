- [« Ds\Vector::reverse](ds-vector.reverse.md)
- [Ds\Vector::rotate »](ds-vector.rotate.md)

- [PHP Manual](index.md)
- [Вектор](class.ds-vector.md)
- Повертає перегорнуту копію вектора

# Ds\Vector::reversed

(PECL ds \>= 1.0.0)

Ds\Vector::reversed — Повертає перевернуту копію вектора

### Опис

public **Ds\Vector::reversed**(): [Ds\Vector](class.ds-vector.md)

Повертає копію вектора.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Перегорнута копія вектора.

> **Примітка**:
>
> Поточний вектор не зміниться.

### Приклади

**Приклад #1 Приклад використання **Ds\Vector::reversed()****

` <?php$vector = new \Ds\Vector(["a", "b", "c"]);print_r($vector->reversed());print_r($vector);?> `

Результатом виконання цього прикладу буде щось подібне:

Ds\Vector Object
(
[0] => c
[1] => b
[2] => a
)
Ds\Vector Object
(
[0] => a
[1] => b
[2] => c
)

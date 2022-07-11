- [« Ds\Vector::get](ds-vector.get.md)
- [Ds\Vector::isEmpty »](ds-vector.isempty.md)

- [PHP Manual](index.md)
- [Вектор](class.ds-vector.md)
- Вставляє значення за вказаним індексом

# Ds\Vector::insert

(PECL ds \>= 1.0.0)

Ds\Vector::insert — Вставляє значення за вказаним індексом

### Опис

public **Ds\Vector::insert**(int `$index`,
[mixed](language.types.declarations.md#language.types.declarations.mixed)
`...$values`): void

Вставляє значення за вказаним індексом.

### Список параметрів

`index`
Індекс, яким необхідно здійснити вставку.
`0 <= index <= count`

> **Примітка**:
>
> Можна вказати індекс, який дорівнює кількості елементів вектора.

`values`
Значення чи значення для вставки.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

Викидає виняток
[OutOfRangeException](class.outofrangeexception.md) у разі
некоректного індексу.

### Приклади

**Приклад #1 Приклад використання **Ds\Vector::insert()****

` <?php$vector = new \Ds\Vector();$vector->insert(0, "e"); // [e]$vector->insert(1, "f"); // [e, f]$vector->insert(2, "g"); // [e, f, g]$vector->insert(0, "a", "b"); // [a, b, e, f, g]$vector->insert(2, ...["c", "d"]); // [a, b, c, d, e, f, g]var_dump($vector);?> `

Результатом виконання цього прикладу буде щось подібне:

object(Ds\Vector)#1 (7) {
[0]=>
string(1) "a"
[1]=>
string(1) "b"
[2]=>
string(1) "c"
[3]=>
string(1) "d"
[4]=>
string(1) "e"
[5]=>
string(1) "f"
[6]=>
string(1) "g"
}

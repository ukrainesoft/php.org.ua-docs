- [« Ds\Vector::shift](ds-vector.shift.md)
- [Ds\Vector::sort »](ds-vector.sort.md)

- [PHP Manual](index.md)
- [Вектор](class.ds-vector.md)
- Повертає підвектор із заданого діапазону

# Ds\Vector::slice

(PECL ds \>= 1.0.0)

Ds\Vector::slice — Повертає підвектор із заданого діапазону

### Опис

public **Ds\Vector::slice**(int `$index`, int `$length` = ?):
[Ds\Vector](class.ds-vector.md)

Повертає підвектор з діапазону заданого початковим індексом `index` та
довжиною `length`.

### Список параметрів

`index`
Індекс, який визначає початок діапазону.

Якщо позитивний, то відраховуватиметься від початку вектора. Якщо
негативний, від кінця.

`length`
Позитивне значення визначає, скільки елементів буде взято. Якщо
кількість елементів вектора менше заданого значення, повернеться стільки
елементів, скільки є. Негативне значення задасть індекс,
відрахований від кінця вектора, що визначає кінець діапазону. Якщо довжина
не задана, то буде повернено всі елементи вектора від заданого індексу
до кінця вектор.

### Значення, що повертаються

Підвектор із заданого діапазону.

### Приклади

**Приклад #1 Приклад використання **Ds\Vector::slice()****

` <?php$vector = new \Ds\Vector(["a", "b", "c", "d", "e"]);// Slice from 2 onwardsprint_r($vector->slice(2) ));// Slice from 1, for a length of 3print_r($vector->slice(1, 3));// Slice from 1 onwardsprint_r($vector->slice(1));// Slice the end onwardsprint_r($vector->slice(-2));// Slice from 1 to 1 from the endprint_r($vector->slice(1, -1));?> `

Результатом виконання цього прикладу буде щось подібне:

Ds\Vector Object
(
[0] => c
[1] => d
[2] => e
)
Ds\Vector Object
(
[0] => b
[1] => c
[2] => d
)
Ds\Vector Object
(
[0] => b
[1] => c
[2] => d
[3] => e
)
Ds\Vector Object
(
[0] => d
[1] => e
)
Ds\Vector Object
(
[0] => b
[1] => c
[2] => d
)

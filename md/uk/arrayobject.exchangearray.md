- [«ArrayObject::count](arrayobject.count.md)
- [ArrayObject::getArrayCopy »](arrayobject.getarraycopy.md)

- [PHP Manual](index.md)
- [ArrayObject](class.arrayobject.md)
- Замінити масив на інший

# ArrayObject::exchangeArray

(PHP 5 \>= 5.1.0, PHP 7, PHP 8)

ArrayObject::exchangeArray — Замінити масив на інший

### Опис

public **ArrayObject::exchangeArray**(array\|object `$array`): array

Замінює поточний масив (array) на інший масив (array) чи об'єкт
(object).

### Список параметрів

`array`
Новий масив (array) чи об'єкт (object) для заміни поточного масиву.

### Значення, що повертаються

Повертає старий масив.

### Приклади

**Приклад #1 Приклад використання **ArrayObject::exchangeArray()****

` <?php// Масив з кількістю фруктів$fruits = array("lemons" => 1, "oranges" => 4, "bananas" => 5, "apples" => 10); $locations = array('Amsterdam', 'Paris', 'London');$fruitsArrayObject = new ArrayObject($fruits);// Зараз замінимо фрукти на місця$old = $fruitsArrayObject $old);print_r($fruitsArrayObject);?> `

Результат виконання цього прикладу:

Array
(
[lemons] => 1
[oranges] => 4
[bananas] => 5
[apples] => 10
)
ArrayObject Object
(
[0] => Amsterdam
[1] => Paris
[2] => London
)

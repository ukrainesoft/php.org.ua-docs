- [«array_pop](function.array-pop.md)
- [array_push »](function.array-push.md)

- [PHP Manual](index.md)
- [Функції для роботи з масивами](ref.array.md)
- Обчислити добуток значень масиву

#array_product

(PHP 5 \>= 5.1.0, PHP 7, PHP 8)

array_product — Обчислити добуток значень масиву

### Опис

**array_product**(array `$array`): int\|float

**array_product()** повертає добуток значень масиву.

### Список параметрів

`array`
Масив.

### Значення, що повертаються

Повертає твір як тип integer або float.

### Приклади

**Приклад #1 Приклади використання **array_product()****

` <?php$a = array(2, 4, 6, 8);echo "product(a) = " . array_product($a) . "
";echo "product(array()) = " . array_product(array()) . "
";?> `

Результат виконання цього прикладу:

product(a) = 384
product(array()) = 1

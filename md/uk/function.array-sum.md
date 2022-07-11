- [«array_splice](function.array-splice.md)
- [array_udiff_assoc »](function.array-udiff-assoc.md)

- [PHP Manual](index.md)
- [Функції для роботи з масивами](ref.array.md)
- обчислює суму значень масиву

#array_sum

(PHP 4 \>= 4.0.4, PHP 5, PHP 7, PHP 8)

array_sum — Обчислює суму значень масиву

### Опис

**array_sum**(array `$array`): int\|float

**array_sum()** повертає суму значень масиву.

### Список параметрів

`array`
Вхідний масив.

### Значення, що повертаються

Повертає суму значень у вигляді цілого числа або числа з плаваючою
точкою; `0`, якщо `array` порожній.

### Приклади

**Приклад #1 Приклад використання **array_sum()****

` <?php$a = array(2, 4, 6, 8);echo "sum(a) = " . array_sum($a) . "
";$b = array("a" => 1.2, "b" => 2.3, c" => 3.4);echo "sum(b) = " . array_sum($b) . "
";?> `

Результат виконання цього прикладу:

sum(a) = 20
sum(b) = 6.9

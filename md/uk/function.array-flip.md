- [«array_filter](function.array-filter.md)
- [array_intersect_assoc »](function.array-intersect-assoc.md)

- [PHP Manual](index.md)
- [Функції для роботи з масивами](ref.array.md)
- Змінює місцями ключі з їхніми значеннями у масиві

#array_flip

(PHP 4, PHP 5, PHP 7, PHP 8)

array_flip — Змінює місцями ключі зі своїми значеннями в масиві

### Опис

**array_flip**(array `$array`): array

Функція **array_flip()** повертає масив (array) навпаки, тобто
ключі масиву `array` стають значеннями, а значення масиву `array`
стають ключами.

Зверніть увагу, що значення масиву `array` мають бути коректними
ключами, тобто вони повинні мати тип int чи string. Якщо значення
має невірний тип, буде видано попередження та дана пара
ключ/значення *не буде включено в результат*.

Якщо значення зустрічається кілька разів, для обробки буде
використовуватися останній зустрінутий ключ, а всі інші будуть
втрачені.

### Список параметрів

`array`
Масив пар, що перевертаються, ключ/значення.

### Значення, що повертаються

Повертає перевернутий масив.

### Приклади

**Приклад #1 Приклад використання **array_flip()****

` <?php$input = array("oranges", "apples", "pears");$flipped = array_flip($input);print_r($flipped);?> `

Результат виконання цього прикладу:

Array
(
[oranges] => 0
[apples] => 1
[pears] => 2
)

**Приклад #2 Приклад використання **array_flip()** з колізіями**

` <?php$input = array("a" => 1, "b" => 1, c" => 2);$flipped = array_flip($input);print_r($flipped);?> `

Результат виконання цього прикладу:

Array
(
[1] => b
[2] => c
)

### Дивіться також

- [array_values()](function.array-values.md) - Вибирає всі значення
масиву
- [array_keys()](function.array-keys.md) - Повертає всі або
деяке підмножина ключів масиву
- [array_reverse()](function.array-reverse.md) - Повертає масив з
елементами у зворотному порядку

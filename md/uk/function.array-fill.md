- [«array_fill_keys](function.array-fill-keys.md)
- [array_filter »](function.array-filter.md)

- [PHP Manual](index.md)
- [Функції для роботи з масивами](ref.array.md)
- Заповнює масив значеннями

#array_fill

(PHP 4 \>= 4.2.0, PHP 5, PHP 7, PHP 8)

array_fill - Заповнює масив значеннями

### Опис

**array_fill**(int `$start_index`, int `$count`,
[mixed](language.types.declarations.md#language.types.declarations.mixed)
`$value`): array

Заповнює масив `count` елементами зі значенням `value`, починаючи з
ключа `start_index`.

### Список параметрів

`start_index`
Перший індекс масиву, що повертається.

Якщо `start_index` негативний, першим індексом масиву, що повертається
буде `start_index`, а наступні індекси починаються з нуля
(дивіться
[Приклад](function.array-fill.md#function.array-fill.example.basic)).

`count`
Кількість елементів, що вставляються. Їх має бути більше або дорівнює нулю.

`value`
Значення для заповнення

### Значення, що повертаються

Повертає заповнений масив

### Помилки

Викликає попередження **`E_WARNING`** у випадку, якщо параметр `count`
меньше нуля.

### Приклади

**Приклад #1 Приклад використання **array_fill()****

` <?php$a = array_fill(5, 6, 'banana');$b = array_fill(-2, 4, 'pear');print_r($a);print_r($b);?> `

Результат виконання цього прикладу:

Array
(
[5] => banana
[6] => banana
[7] => banana
[8] => banana
[9] => banana
[10] => banana
)
Array
(
[-2] => pear
[0] => pear
[1] => pear
[2] => pear
)

### Примітки

Дивіться також докладний опис негативних ключів у розділі [Масиви](language.types.array.md).

### Дивіться також

- [array_fill_keys()](function.array-fill-keys.md) - Створює масив
та заповнює його значеннями з певними ключами
- [str_repeat()](function.str-repeat.md) - Повертає повторювану
рядок
- [range()](function.range.md) - Створює масив, що містить діапазон
елементів

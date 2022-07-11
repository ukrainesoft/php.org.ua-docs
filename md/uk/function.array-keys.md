- [«array_key_last](function.array-key-last.md)
- [array_map »](function.array-map.md)

- [PHP Manual](index.md)
- [Функції для роботи з масивами](ref.array.md)
- Повертає всі або деякі підмножини ключів масиву

#array_keys

(PHP 4, PHP 5, PHP 7, PHP 8)

array_keys — Повертає всі або деякі підмножини ключів масиву

### Опис

**array_keys**(array `$array`): array

**array_keys**(array `$array`,
[mixed](language.types.declarations.md#language.types.declarations.mixed)
`$search_value`, bool `$strict` = **`false`**): array

Функція **array_keys()** повертає числові та рядкові ключі,
що містяться в масиві `array`.

Якщо вказано параметр `search_value`, функція повертає ключі, у яких
Значення елементів масиву збігаються з цим параметром. У зворотному
У випадку, функція повертає всі ключі масиву `array`.

### Список параметрів

`array`
Масив, що містить ключі, що повертаються.

`search_value`
Якщо зазначено, будуть повернені тільки ключі, які мають значення елементів
масиву збігаються з цим параметром.

`strict`
Визначає використання суворої перевірки рівності (===) під час пошуку.

### Значення, що повертаються

Повертає масив з усіма ключами `array`.

### Приклади

**Приклад #1 Приклад використання **array_keys()****

` <?php$array = array(0 => 100, "color" => "red");print_r(array_keys($array));$array = array("blue", "red", "green", "blue", "blue");print_r(array_keys($array, "blue"));$array = array("color" => array("blue", "red", "green"),            => array("small", "medium", "large"));print_r(array_keys($array));?> `

Результат виконання цього прикладу:

Array
(
[0] => 0
[1] => color
)
Array
(
[0] => 0
[1] => 3
[2] => 4
)
Array
(
[0] => color
[1] => size
)

### Дивіться також

- [array_values()](function.array-values.md) - Вибирає всі значення
масиву
- [array_combine()](function.array-combine.md) - Створює новий
масив, використовуючи один масив як ключі, а інший для нього
значень
- [array_key_exists()](function.array-key-exists.md) - Перевіряє,
чи присутній у масиві зазначений ключ чи індекс
- [array_search()](function.array-search.md) - Пошук
даного значення в масиві та повертає ключ першого знайденого
елемента у разі успішного виконання

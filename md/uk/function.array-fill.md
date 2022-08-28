Заповнює масив значеннями

-   [« array\_fill\_keys](function.array-fill-keys.html)
    
-   [array\_filter »](function.array-filter.html)
    
-   [PHP Manual](index.html)
    
-   [Функции для работы с массивами](ref.array.html)
    
-   Заповнює масив значеннями
    

# arrayfill

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

arrayfill - Заповнює масив значеннями

### Опис

```methodsynopsis
array_fill(int $start_index, int $count, mixed $value): array
```

Заповнює масив `count` елементами зі значенням `value`, починаючи з ключа `start_index`

### Список параметрів

`start_index`

Перший індекс масива, що повертається.

Якщо `start_index` негативний, першим індексом масиву, що повертається `start_index`, а наступні індекси починаються з нуля (дивіться [пример](function.array-fill.html#function.array-fill.example.basic)

`count`

Кількість елементів, що додаються. Повинно бути більше або одно нулю і менше чи одно `2147483647`

`value`

Значення заповнення.

### Значення, що повертаються

Повертає заповнений масив.

### Помилки

Викидає виняток [ValueError](class.valueerror.html) у випадку, якщо параметр `count` виходить за межі діапазону.

### список змін

| Версия | Описание |
| --- | --- |
|  | Функція **arrayfill()** тепер викидає виняток [ValueError](class.valueerror.html), якщо параметр `count` виходить за межі діапазону; раніше видавалася помилка рівня **`E_WARNING`**, а функція повертала значення **`false`** |

### Приклади

**Приклад #1 Приклад використання **arrayfill()****

```php
<?php
$a = array_fill(5, 6, 'banana');
$b = array_fill(-2, 4, 'pear');
print_r($a);
print_r($b);
?>
```

Результат виконання цього прикладу:

```
Array
(
    [5]  => banana
    [6]  => banana
    [7]  => banana
    [8]  => banana
    [9]  => banana
    [10] => banana
)
Array
(
    [-2] => pear
    [0] => pear
    [1] => pear
    [2] => pear
)
```

### Примітки

Дивіться також докладний опис негативних ключів у розділі [Массивы](language.types.array.html)

### Дивіться також

-   [array\_fill\_keys()](function.array-fill-keys.html) - створює масив і заповнює його значеннями з певними ключами
-   [str\_repeat()](function.str-repeat.html) - Повертає рядок, що повторюється
-   [range()](function.range.html) - Створює масив, що містить діапазон елементів
---
navigation:
  - function.array-key-last.md: « arraykeylast
  - function.array-map.md: arraymap »
  - index.md: PHP Manual
  - ref.array.md: Функції для роботи з масивами
title: arraykeys
---
# arraykeys

(PHP 4, PHP 5, PHP 7, PHP 8)

arraykeys — Повертає всі або деякі підмножини ключів масиву

### Опис

```methodsynopsis
array_keys(array $array): array
```

```methodsynopsis
array_keys(array $array, mixed $search_value, bool $strict = false): array
```

Функція **arraykeys()** повертає числові та рядкові ключі, що містяться в масиві `array`

Якщо вказано параметр `search_value`, функція повертає ключі, у яких значення елементів масиву збігаються з цим параметром. В іншому випадку, функція повертає всі ключі масиву `array`

### Список параметрів

`array`

Масив, що містить ключі, що повертаються.

`search_value`

Якщо вказано, буде повернено лише ключі, у яких значення елементів масиву збігаються з цим параметром.

`strict`

Визначає використання суворої перевірки рівності (===) під час пошуку.

### Значення, що повертаються

Повертає масив із усіма ключами `array`

### Приклади

**Приклад #1 Приклад використання **arraykeys()****

```php
<?php
$array = array(0 => 100, "color" => "red");
print_r(array_keys($array));

$array = array("blue", "red", "green", "blue", "blue");
print_r(array_keys($array, "blue"));

$array = array("color" => array("blue", "red", "green"),
               "size"  => array("small", "medium", "large"));
print_r(array_keys($array));
?>
```

Результат виконання цього прикладу:

```
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
```

### Дивіться також

-   [arrayvalues()](function.array-values.md) - Вибирає всі значення масиву
-   [arraycombine()](function.array-combine.md) - Створює новий масив, використовуючи один масив як ключі, а інший для його значень
-   [arraykeyexists()](function.array-key-exists.md) - Перевіряє, чи присутній у масиві зазначений ключ чи індекс
-   [arraysearch()](function.array-search.md) - Здійснює пошук даного значення в масиві та повертає ключ першого знайденого елемента у разі успішного виконання

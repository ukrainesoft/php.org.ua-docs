---
navigation:
  - function.array-key-last.md: « array\_key\_last
  - function.array-map.md: array\_map »
  - index.md: PHP Manual
  - ref.array.md: Функції для роботи з масивами
title: array\_keys
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# array\_keys

(PHP 4, PHP 5, PHP 7, PHP 8)

array\_keys — Повертає всі або деякі підмножини ключів масиву

### Опис

```methodsynopsis
array_keys(array $array): array
```

```methodsynopsis
array_keys(array $array, mixed $filter_value, bool $strict = false): array
```

Функция**array\_keys()** повертає числові та рядкові ключі, що містяться в масиві `array`

Если указан параметр`filter_value`, функція повертає ключі, у яких значення елементів масиву збігаються з цим параметром. В іншому випадку, функція повертає всі ключі масиву `array`

### Список параметрів

`array`

Масив, що містить ключі, що повертаються.

`filter_value`

Якщо вказано, буде повернено лише ключі, у яких значення елементів масиву збігаються з цим параметром.

`strict`

Визначає використання суворої перевірки рівності (===) під час пошуку.

### Значення, що повертаються

Повертає масив з усіма ключами `array`

### Приклади

**Приклад #1 Приклад використання** array\_keys()\*\*\*\*

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

Результат виконання наведеного прикладу:

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

-   [array\_values()](function.array-values.md) \- Повертає всі значення масиву
-   [array\_combine()](function.array-combine.md) \- Створює новий масив, використовуючи один масив як ключі, а інший для його значень
-   [array\_key\_exists()](function.array-key-exists.md) \- Перевіряє, чи існує в масиві заданий ключ чи індекс
-   [array\_search()](function.array-search.md) \- Здійснює пошук даного значення в масиві та повертає ключ першого знайденого елемента у разі успішного виконання

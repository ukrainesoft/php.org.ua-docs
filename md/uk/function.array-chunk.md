---
navigation:
  - function.array-change-key-case.md: « array\_change\_key\_case
  - function.array-column.md: array\_column »
  - index.md: PHP Manual
  - ref.array.md: Функції для роботи з масивами
title: array\_chunk
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# array\_chunk

(PHP 4 >= 4.2.0, PHP 5, PHP 7, PHP 8)

array\_chunk - Розбиває масив на частини

### Опис

```methodsynopsis
array_chunk(array $array, int $length, bool $preserve_keys = false): array
```

Розбиває масив на масиви із заданим у параметрі `length` кількістю елементів. Кількість елементів в останній частині дорівнюватиме або виявиться меншою за задану довжину (`length`

### Список параметрів

`array`

Масив, який треба розбити.

`length`

Розміри кожної частини.

`preserve_keys`

Если установлено значение\*\*`true`\*\*, ключі оригінального масиву будуть збережені. За замовчуванням - **`false`**, що переіндексує частини числовими ключами

### Значення, що повертаються

Повертає багатовимірний індексний масив (індексація починається з нуля), у якому кожен елемент першого рівня містить `length` елементів.

### Помилки

Якщо параметр `length`меньше , буде викинуто виняток [ValueError](class.valueerror.md)

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Якщо параметр `length`меньше , буде викинуто виняток [ValueError](class.valueerror.md); раніше, натомість видавалася помилка рівня **`E_WARNING`** та функція повертала **`null`** |

### Приклади

**Пример #1 Пример использования функции**array\_chunk()\*\*\*\*

```php
<?php

$input_array = array('a', 'b', 'c', 'd', 'e');
print_r(array_chunk($input_array, 2));
print_r(array_chunk($input_array, 2, true));
?>
```

Результат виконання наведеного прикладу:

```
Array
(
    [0] => Array
        (
            [0] => a
            [1] => b
        )

    [1] => Array
        (
            [0] => c
            [1] => d
        )

    [2] => Array
        (
            [0] => e
        )

)
Array
(
    [0] => Array
        (
            [0] => a
            [1] => b
        )

    [1] => Array
        (
            [2] => c
            [3] => d
        )

    [2] => Array
        (
            [4] => e
        )

)
```

### Дивіться також

-   [array\_slice()](function.array-slice.md) \- Вибирає зріз масиву

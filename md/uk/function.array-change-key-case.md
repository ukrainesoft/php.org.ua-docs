---
navigation:
  - ref.array.md: « Функції для роботи з масивами
  - function.array-chunk.html: arraychunk »
  - index.md: PHP Manual
  - ref.array.md: Функції для роботи з масивами
title: arraychangekeycase
---
# arraychangekeycase

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

arraychangekeycase — Змінює регістр усіх ключів у масиві

### Опис

```methodsynopsis
array_change_key_case(array $array, int $case = CASE_LOWER): array
```

Повертає масив `array`, всі ключі якого перетворені на нижній або верхній регістр. Числові ключі залишаться недоторканими.

### Список параметрів

`array`

Оброблюваний масив

`case`

Або **`CASE_UPPER`**, або **`CASE_LOWER`** (використовується за замовчуванням)

### Значення, що повертаються

Повертає масив з ключами, перетвореними на верхній або нижній регістр, або **`null`**, якщо `array` не є масивом.

### Помилки

Генерує помилку рівня **`E_WARNING`**, якщо `array` не є масивом.

### Приклади

**Приклад #1 Приклад використання **arraychangekeycase()****

```php
<?php
$input_array = array("FirSt" => 1, "SecOnd" => 4);
print_r(array_change_key_case($input_array, CASE_UPPER));
?>
```

Результат виконання цього прикладу:

```
Array
(
    [FIRST] => 1
    [SECOND] => 4
)
```

### Примітки

> **Зауваження**
> 
> Якщо масив містить індекси, які стануть однойменними після застосування цієї функції (наприклад, "`keY`"і"`kEY`"), значення останнього однойменного індексу перекриє інші збігаються значення цього масиву.

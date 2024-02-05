---
navigation:
  - ref.array.md: « Функції для роботи з масивами
  - function.array-chunk.md: array\_chunk »
  - index.md: PHP Manual
  - ref.array.md: Функції для роботи з масивами
title: array\_change\_key\_case
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# array\_change\_key\_case

(PHP 4 >= 4.2.0, PHP 5, PHP 7, PHP 8)

array\_change\_key\_case — Змінює регістр усіх ключів у масиві

### Опис

```methodsynopsis
array_change_key_case(array $array, int $case = CASE_LOWER): array
```

Повертає масив `array`, всі ключі якого перетворені на нижній або верхній регістр. Числові ключі залишаться недоторканими.

### Список параметрів

`array`

Оброблюваний масив

`case`

Либо\*\*`CASE_UPPER`**, либо**`CASE_LOWER`\*\*(используется по умолчанию)

### Значення, що повертаються

Повертає масив із ключами, перетвореними у верхній або нижній регістр.

### Приклади

**Пример #1 Пример использования**array\_change\_key\_case()\*\*\*\*

```php
<?php
$input_array = array("FirSt" => 1, "SecOnd" => 4);
print_r(array_change_key_case($input_array, CASE_UPPER));
?>
```

Результат виконання наведеного прикладу:

```
Array
(
    [FIRST] => 1
    [SECOND] => 4
)
```

### Примітки

> **Зауваження** :
> 
> Якщо масив містить індекси, які стануть однойменними після застосування цієї функції (наприклад, "`keY`"і"`kEY`"), значення останнього однойменного індексу перекриє інші збігаються значення цього масиву.

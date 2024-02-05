---
navigation:
  - function.filter-input.md: « filter\_input
  - function.filter-var-array.md: filter\_var\_array »
  - index.md: PHP Manual
  - ref.filter.md: Функції фільтрації даних
title: filter\_list
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# filter\_list

(PHP 5 >= 5.2.0, PHP 7, PHP 8)

filter\_list — Повертає список усіх підтримуваних фільтрів

### Опис

```methodsynopsis
filter_list(): array
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає масив імен усіх фільтрів, що підтримуються, порожній масив, якщо таких фільтрів не існує. Ідентифікатори (ID) фільтрів не є ключами цього масиву, вони можуть бути отримані за допомогою функції [filter\_id()](function.filter-id.md)по имени фильтра.

### Приклади

**Приклад #1 Приклад використання** filter\_list()\*\*\*\*

```php
<?php
print_r(filter_list());
?>
```

Висновок наведеного прикладу буде схожим на:

```
Array
(
    [0] => int
    [1] => boolean
    [2] => float
    [3] => validate_regexp
    [4] => validate_url
    [5] => validate_email
    [6] => validate_ip
    [7] => string
    [8] => stripped
    [9] => encoded
    [10] => special_chars
    [11] => unsafe_raw
    [12] => email
    [13] => url
    [14] => number_int
    [15] => number_float
    [16] => magic_quotes
    [17] => callback
)
```

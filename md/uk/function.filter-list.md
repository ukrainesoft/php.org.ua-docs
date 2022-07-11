- [«filter_input](function.filter-input.md)
- [filter_var_array »](function.filter-var-array.md)

- [PHP Manual](index.md)
- [Функції фільтрації даних](ref.filter.md)
- Повертає список усіх підтримуваних фільтрів

#filter_list

(PHP 5 \>= 5.2.0, PHP 7, PHP 8)

filter_list — Повертає список усіх підтримуваних фільтрів

### Опис

**filter_list**(): array

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає масив імен усіх підтримуваних фільтрів, порожній масив, якщо
таких фільтрів немає. Ідентифікатори (ID) фільтрів не є
ключами цього масиву вони можуть бути отримані за допомогою функції
[filter_id()](function.filter-id.md) на ім'я фільтра.

### Приклади

**Приклад #1 Приклад використання **filter_list()****

` <?phpprint_r(filter_list());?> `

Результатом виконання цього прикладу буде щось подібне:

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

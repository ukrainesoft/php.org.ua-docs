---
navigation:
  - function.is-double.md: « is\_double
  - function.is-int.md: is\_int »
  - index.md: PHP Manual
  - ref.var.md: Функції для роботи зі змінними
title: is\_float
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# is\_float

(PHP 4, PHP 5, PHP 7, PHP 8)

is\_float — Перевіряє, чи є змінна кількість з плаваючою точкою

### Опис

```methodsynopsis
is_float(mixed $value): bool
```

Перевіряє, чи є змінна число з плаваючою точкою.

> **Зауваження** :
> 
> Щоб перевірити належність змінної до чи числовому рядку (наприклад, при обробці полів введення форми, які завжди передаються у вигляді рядка), викликають функцію [is\_numeric()](function.is-numeric.md)

### Список параметрів

`value`

Перевірена змінна.

### Значення, що повертаються

Повертає **`true`**, если значение`value` - Число з плаваючою точкою (float), інакше **`false`**

### Приклади

**Приклад #1 Приклад использования функции**is\_float()\*\*\*\*

```php
<?php

var_dump(is_float(27.25));
var_dump(is_float('abc'));
var_dump(is_float(23));
var_dump(is_float(23.5));
var_dump(is_float(1e7));  //Научная нотация
var_dump(is_float(true));

?>
```

Результат виконання наведеного прикладу:

```
bool(true)
bool(false)
bool(false)
bool(true)
bool(true)
bool(false)
```

### Дивіться також

-   [is\_bool()](function.is-bool.md) \- Перевіряє, чи є змінна логічне значення
-   [is\_int()](function.is-int.md) \- Перевіряє, чи є змінна ціла кількість
-   [is\_numeric()](function.is-numeric.md) \- Перевіряє, чи містить змінне число чи числове рядок
-   [is\_string()](function.is-string.md) \- Перевіряє, чи є тип змінної рядок
-   [is\_array()](function.is-array.md) \- Визначає, чи є змінна масив
-   [is\_object()](function.is-object.md) \- Перевіряє, чи є змінна об'єкт

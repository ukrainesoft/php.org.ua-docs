---
navigation:
  - function.is-float.md: « is\_float
  - function.is-integer.md: is\_integer »
  - index.md: PHP Manual
  - ref.var.md: Функції для роботи зі змінними
title: is\_int
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# is\_int

(PHP 4, PHP 5, PHP 7, PHP 8)

is\_int — Перевіряє, чи є змінна ціла кількість

### Опис

```methodsynopsis
is_int(mixed $value): bool
```

Перевіряє, чи належить тип змінної цілого числа (int).

> **Зауваження** :
> 
> Щоб перевірити належність змінної до чи числовому рядку (наприклад, при обробці полів введення форми, які завжди передаються у вигляді рядка), викликають функцію [is\_numeric()](function.is-numeric.md)

### Список параметрів

`value`

Перевірена змінна.

### Значення, що повертаються

Повертає **`true`**, если значение`value` - ціле число (int), інакше **`false`**

### Приклади

**Пример #1 Пример использования функции**is\_int()\*\*\*\*

```php
<?php

$values = array(23, "23", 23.5, "23.5", null, true, false);
foreach ($values as $value) {
    echo "is_int(";
    var_export($value);
    echo ") = ";
    var_dump(is_int($value));
}

?>
```

Результат виконання наведеного прикладу:

```
is_int(23) = bool(true)
is_int('23') = bool(false)
is_int(23.5) = bool(false)
is_int('23.5') = bool(false)
is_int(NULL) = bool(false)
is_int(true) = bool(false)
is_int(false) = bool(false)
```

### Дивіться також

-   [is\_bool()](function.is-bool.md) \- Перевіряє, чи є змінна логічне значення
-   [is\_float()](function.is-float.md) \- Перевіряє, чи є змінна число з плаваючою точкою
-   [is\_numeric()](function.is-numeric.md) \- Перевіряє, чи містить змінне число чи числове рядок
-   [is\_string()](function.is-string.md) \- Перевіряє, чи є тип змінної рядок
-   [is\_array()](function.is-array.md) \- Визначає, чи є змінна масив
-   [is\_object()](function.is-object.md) \- Перевіряє, чи є змінна об'єкт

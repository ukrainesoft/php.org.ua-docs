---
navigation:
  - function.is-scalar.md: « is\_scalar
  - function.isset.md: isset »
  - index.md: PHP Manual
  - ref.var.md: Функції для роботи зі змінними
title: is\_string
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# is\_string

(PHP 4, PHP 5, PHP 7, PHP 8)

is\_string — Перевіряє, чи є тип змінної рядок

### Опис

```methodsynopsis
is_string(mixed $value): bool
```

Перевіряє, чи є тип змінної рядок.

### Список параметрів

`value`

Перевірена змінна.

### Значення, що повертаються

Повертає **`true`**, если значение`value` - Рядок, інакше **`false`**

### Приклади

**Приклад #1 Приклад использования функции**is\_string()\*\*\*\*

```php
<?php

$values = array(false, true, null, 'abc', '23', 23, '23.5', 23.5, '', ' ', '0', 0);
foreach ($values as $value) {
    echo "is_string(";
    var_export($value);
    echo ") = ";
    echo var_dump(is_string($value));
}

?>
```

Результат виконання наведеного прикладу:

```
is_string(false) = bool(false)
is_string(true) = bool(false)
is_string(NULL) = bool(false)
is_string('abc') = bool(true)
is_string('23') = bool(true)
is_string(23) = bool(false)
is_string('23.5') = bool(true)
is_string(23.5) = bool(false)
is_string('') = bool(true)
is_string(' ') = bool(true)
is_string('0') = bool(true)
is_string(0) = bool(false)
```

### Дивіться також

-   [is\_float()](function.is-float.md) \- Перевіряє, чи є змінна число з плаваючою точкою
-   [is\_int()](function.is-int.md) \- Перевіряє, чи є змінна ціла кількість
-   [is\_bool()](function.is-bool.md) \- Перевіряє, чи є змінна логічне значення
-   [is\_object()](function.is-object.md) \- Перевіряє, чи є змінна об'єкт
-   [is\_array()](function.is-array.md) \- Визначає, чи є змінна масив

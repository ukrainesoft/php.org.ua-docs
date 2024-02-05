---
navigation:
  - function.is-null.md: « is\_null
  - function.is-object.md: is\_object »
  - index.md: PHP Manual
  - ref.var.md: Функції для роботи зі змінними
title: is\_numeric
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# is\_numeric

(PHP 4, PHP 5, PHP 7, PHP 8)

is\_numeric — Перевіряє, чи містить змінне число або числове рядок

### Опис

```methodsynopsis
is_numeric(mixed $value): bool
```

Визначає, чи є змінна число або [рядок, що містить число](language.types.numeric-strings.md)

### Список параметрів

`value`

Перевірена змінна.

### Значення, що повертаються

Повертає **`true`**, если значение`value` - Число або [рядок, що містить число](language.types.numeric-strings.md), иначе\*\*`false`\*\*

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Рядки, що складаються з чисел і закінчуються пробілом (`«42 »`), тепер повертатимуть **`true`**. . Раніше натомість поверталося **`false`** |

### Приклади

**Приклад #1 Приклад використання функції **is\_numeric()****

```php
<?php

$tests = array(
    "42",
    1337,
    0x539,
    02471,
    0b10100111001,
    1337e0,
    "0x539",
    "02471",
    "0b10100111001",
    "1337e0",
    "not numeric",
    array(),
    9.1,
    null,
    '',
);

foreach ($tests as $element) {
    if (is_numeric($element)) {
        echo var_export($element, true) . " число", PHP_EOL;
    } else {
        echo var_export($element, true) . " НЕ число", PHP_EOL;
    }
}

?>
```

Результат виконання наведеного прикладу:

```
42 - число
1337 - число
1337 - число
1337 - число
1337 - число
1337.0 - число
'0x539' - НЕ число
'02471' - число
'0b10100111001' - НЕ число
'1337e0' - число
'not numeric' - НЕ число
array (
) - НЕ число
9.1 - число
NULL - НЕ число
'' - НЕ число
```

**Пример #2 Пример использования функции**is\_numeric()\*\* з пропуском\*\*

```php
<?php

$tests = [
    " 42",
    "42 ",
    "\u{A0}9001", // Неразрывный пробел
    "9001\u{A0}", // Неразрывный пробел
];
foreach ($tests as $element) {
    if (is_numeric($element)) {
        echo var_export($element, true) . " — число", PHP_EOL;
    } else {
        echo var_export($element, true) . " — НЕ число", PHP_EOL;
    }
}

?>
```

Результат виконання наведеного прикладу в PHP 8:

```
' 42' — число
'42 ' — число
' 9001' — НЕ число
'9001 ' — НЕ число
```

Результат виконання наведеного прикладу в PHP 7:

```
' 42' — число
'42 ' — НЕ число
' 9001' — НЕ число
'9001 ' — НЕ число
```

### Дивіться також

-   [Рядки, що містять числа](language.types.numeric-strings.md)
-   [ctype\_digit()](function.ctype-digit.md) \- Перевіряє цифрові символи
-   [is\_bool()](function.is-bool.md) \- Перевіряє, чи є змінна логічне значення
-   [is\_null()](function.is-null.md) \- Перевіряє, чи значення змінної null дорівнює
-   [is\_float()](function.is-float.md) \- Перевіряє, чи є змінна число з плаваючою точкою
-   [is\_int()](function.is-int.md) \- Перевіряє, чи є змінна ціла кількість
-   [is\_string()](function.is-string.md) \- Перевіряє, чи є тип змінної рядок
-   [is\_object()](function.is-object.md) \- Перевіряє, чи є змінна об'єкт
-   [is\_array()](function.is-array.md) \- Визначає, чи є змінна масив
-   [filter\_var()](function.filter-var.md) \- Фільтрує змінну за допомогою певного фільтра

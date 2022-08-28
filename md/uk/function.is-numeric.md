Перевіряє, чи є змінна числом або рядком, що містить число

-   [« is\_null](function.is-null.html)
    
-   [is\_object »](function.is-object.html)
    
-   [PHP Manual](index.html)
    
-   [Функции для работы с переменными](ref.var.html)
    
-   Перевіряє, чи є змінна числом або рядком, що містить число
    

# ісnumeric

(PHP 4, PHP 5, PHP 7, PHP 8)

ісnumeric — Перевіряє, чи є змінна числом або рядком, що містить число

### Опис

```methodsynopsis
is_numeric(mixed $value): bool
```

Визначає, чи є ця змінна числом чи [строкой, содержащей число](language.types.numeric-strings.html)

### Список параметрів

`value`

Перевірена змінна.

### Значення, що повертаються

Повертає **`true`**, якщо `value` є числом або [строкой, содержащей число](language.types.numeric-strings.html) або **`false`** в іншому випадку.

### список змін

| Версия | Описание |
| --- | --- |
|  | Рядки, що складаються з чисел, що закінчуються пробілом (`"42 "`), тепер повертатимуть **`true`**. Раніше натомість поверталося **`false`** |

### Приклади

**Приклад #1 Приклади використання **ісnumeric()****

```php
<?php
$tests = array(
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
    "not numeric",
    array(),
    9.1,
    null,
    '',
);

foreach ($tests as $element) {
    if (is_numeric($element)) {
        echo var_export($element, true) . " is numeric", PHP_EOL;
    } else {
        echo var_export($element, true) . " is NOT numeric", PHP_EOL;
    }
}
?>
```

Результат виконання цього прикладу:

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

**Приклад #2 Приклад використання **ісnumeric()** з пропуском**

```php
<?php
$tests = [
    " 42",
    "42 ",
    " 9001", // неразрывный пробел
    "9001 ", // неразрывный пробел
];
foreach ($tests as $element) {
    if (is_numeric($element)) {
        echo var_export($element, true) . " - число", PHP_EOL;
    } else {
        echo var_export($element, true) . " - НЕ число", PHP_EOL;
    }
}
?>
```

Результат виконання цього прикладу в PHP 8:

```
' 42' - число
'42 ' - число
' 9001' - НЕ число
'9001 ' - НЕ число
```

Результат виконання цього прикладу в PHP 7:

```
' 42' - число
'42 ' - НЕ число
' 9001' - НЕ число
'9001 ' - НЕ число
```

### Дивіться також

-   [Строки, содержащие числа](language.types.numeric-strings.html)
-   [ctype\_digit()](function.ctype-digit.html) - Перевіряє наявність цифрових символів у рядку
-   [is\_bool()](function.is-bool.html) - Перевіряє, чи є змінна булевою
-   [is\_null()](function.is-null.html) - Перевіряє, чи значення змінної дорівнює null
-   [is\_float()](function.is-float.html) - Перевіряє, чи є змінна числом із плаваючою точкою
-   [is\_int()](function.is-int.html) - Перевіряє, чи є змінна цілим числом
-   [is\_string()](function.is-string.html) - Перевіряє, чи є змінним рядком
-   [is\_object()](function.is-object.html) - Перевіряє, чи є змінна об'єктом
-   [is\_array()](function.is-array.html) - Визначає, чи є змінна масивом
-   [filter\_var()](function.filter-var.html) - Фільтрує змінну за допомогою певного фільтра
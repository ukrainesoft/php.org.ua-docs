---
navigation:
  - function.quotemeta.md: « quotemeta
  - function.setlocale.md: setlocale »
  - index.md: PHP Manual
  - ref.strings.md: Функції для роботи з рядками
title: rtrim
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# rtrim

(PHP 4, PHP 5, PHP 7, PHP 8)

rtrim — Видалення пробілів (або інших символів) з кінця рядка

### Опис

```methodsynopsis
rtrim(string $string, string $characters = " \n\r\t\v\x00"): string
```

Ця функція повертає рядок `string` із віддаленими з кінця рядка пробіловими (або іншими) символами.

Якщо другий параметр не передано, **rtrim()** видаляє такі символи:

-   " " (ASCII `32` `0x20`)), звичайний пробіл.
-   "\\t" (ASCII `9` `0x09`)), символ табуляції.
-   "\\n" (ASCII `10` `0x0A`)), символ перекладу рядка.
-   "\\r" (ASCII `13` `0x0D`)), символ повернення каретки.
-   "\\0" (ASCII `0x00`)), `NULL`\-байт.
-   "\\v" (ASCII `11` `0x0B`)), вертикальна табуляція.

### Список параметрів

`string`

Вхідний рядок.

`characters`

С помощью параметра`characters` можна також вказати символи, що видаляються. Просто перерахуйте всі символи, які потрібно видалити. Можна вказати конструкцію `.. .` для обозначения диапазона символов.

### Значення, що повертаються

Повертає модифікований рядок.

### Приклади

**Приклад #1 Приклад використання** rtrim()\*\*\*\*

```php
<?php

$text = "\t\tThese are a few words :) ...  ";
$binary = "\x09Example string\x0A";
$hello  = "Hello World";
var_dump($text, $binary, $hello);

print "\n";

$trimmed = rtrim($text);
var_dump($trimmed);

$trimmed = rtrim($text, " \t.");
var_dump($trimmed);

$trimmed = rtrim($hello, "Hdle");
var_dump($trimmed);

// удаляем управляющие ASCII-символы с конца $binary
// (от 0 до 31 включительно)
$clean = rtrim($binary, "\x00..\x1F");
var_dump($clean);

?>
```

Результат виконання наведеного прикладу:

```
string(32) "        These are a few words :) ...  "
string(16) "    Example string
"
string(11) "Hello World"

string(30) "        These are a few words :) ..."
string(26) "        These are a few words :)"
string(9) "Hello Wor"
string(15) "    Example string"
```

### Дивіться також

-   [trim()](function.trim.md) \- Видаляє прогалини (або інші символи) з початку та кінця рядка
-   [ltrim()](function.ltrim.md) \- Видаляє прогалини (або інші символи) з початку рядка

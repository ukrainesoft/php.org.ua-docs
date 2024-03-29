---
navigation:
  - function.localeconv.md: « localeconv
  - function.md5-file.md: md5\_file »
  - index.md: PHP Manual
  - ref.strings.md: Функції для роботи з рядками
title: ltrim
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ltrim

(PHP 4, PHP 5, PHP 7, PHP 8)

ltrim — Видалення пробілів (або інших символів) з початку рядка

### Опис

```methodsynopsis
ltrim(string $string, string $characters = " \n\r\t\v\x00"): string
```

Видаляє пробіли (або інші символи) з початку рядка.

### Список параметрів

`string`

Вхідний рядок.

`characters`

С помощью параметра`characters` можна також вказати символи, що видаляються. Просто перерахуйте всі символи, які потрібно видалити. Можна вказати конструкцію `.. .` для обозначения диапазона символов.

### Значення, що повертаються

Ця функція повертає рядок `string` з віддаленими з початку рядка пробілами. Якщо другий параметр не передано, **ltrim()** видаляє такі символи:

-   " " (ASCII `32` `0x20`)), звичайний пробіл.
-   "\\t" (ASCII `9` `0x09`)), символ табуляції.
-   "\\n" (ASCII `10` `0x0A`)), символ перекладу рядка.
-   "\\r" (ASCII `13` `0x0D`)), символ повернення каретки.
-   "\\0" (ASCII `0x00`)), `NUL`\-байт.
-   "\\v" (ASCII `11` `0x0B`)), вертикальна табуляція.

### Приклади

**Приклад #1 Приклад використання** ltrim()\*\*\*\*

```php
<?php

$text = "\t\tThese are a few words :) ...  ";
$binary = "\x09Example string\x0A";
$hello  = "Hello World";
var_dump($text, $binary, $hello);

print "\n";


$trimmed = ltrim($text);
var_dump($trimmed);

$trimmed = ltrim($text, " \t.");
var_dump($trimmed);

$trimmed = ltrim($hello, "Hdle");
var_dump($trimmed);

// удаляем управляющие ASCII-символы с начала $binary
// (от 0 до 31 включительно)
$clean = ltrim($binary, "\x00..\x1F");
var_dump($clean);

?>
```

Результат виконання наведеного прикладу:

```
string(32) "        These are a few words :) ...  "
string(16) "    Example string
"
string(11) "Hello World"

string(30) "These are a few words :) ...  "
string(30) "These are a few words :) ...  "
string(7) "o World"
string(15) "Example string
"
```

### Дивіться також

-   [trim()](function.trim.md) \- Видаляє прогалини (або інші символи) з початку та кінця рядка
-   [rtrim()](function.rtrim.md) \- Видаляє прогалини (або інші символи) з кінця рядка

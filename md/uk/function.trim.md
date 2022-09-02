---
navigation:
  - function.substr.md: « substr
  - function.ucfirst.md: ucfirst »
  - index.md: PHP Manual
  - ref.strings.md: Функції для роботи з рядками
title: trim
---
# trim

(PHP 4, PHP 5, PHP 7, PHP 8)

trim — Видалення пробілів (або інших символів) з початку та кінця рядка

### Опис

```methodsynopsis
trim(string $string, string $characters = " \n\r\t\v\x00"): string
```

Ця функція повертає рядок `string` з віддаленими з початку та кінця рядка пробілами. Якщо другий параметр не передано, **trim()** видаляє такі символи:

-   " " (ASCII `32` `0x20`)), звичайний пробіл.
-   "t" (ASCII `9` `0x09`)), символ табуляції.
-   "n" (ASCII `10` `0x0A`)), символ перекладу рядка.
-   "r" (ASCII `13` `0x0D`)), символ повернення каретки.
-   "0" (ASCII `0` `0x00` `NUL`байт.
-   "v" (ASCII `11` `0x0B`)), вертикальна табуляція.

### Список параметрів

`string`

Обрізний рядок (string).

`characters`

Можна також встановити список символів для видалення за допомогою необов'язкового аргументу `characters`. Просто перерахуйте всі символи, які потрібно видалити. Можна вказати конструкцію `..` для позначення діапазону символів.

### Значення, що повертаються

Обрізний рядок.

### Приклади

**Приклад #1 Приклад використання **trim()****

```php
<?php

$text   = "\t\tThese are a few words :) ...  ";
$binary = "\x09Example string\x0A";
$hello  = "Hello World";
var_dump($text, $binary, $hello);

print "\n";

$trimmed = trim($text);
var_dump($trimmed);

$trimmed = trim($text, " \t.");
var_dump($trimmed);

$trimmed = trim($hello, "Hdle");
var_dump($trimmed);

$trimmed = trim($hello, 'HdWr');
var_dump($trimmed);

// удаляем управляющие ASCII-символы с начала и конца $binary
// (от 0 до 31 включительно)
$clean = trim($binary, "\x00..\x1F");
var_dump($clean);

?>
```

Результат виконання цього прикладу:

```
string(32) "        These are a few words :) ...  "
string(16) "    Example string
"
string(11) "Hello World"

string(28) "These are a few words :) ..."
string(24) "These are a few words :)"
string(5) "o Wor"
string(9) "ello Worl"
string(14) "Example string"
```

**Приклад #2 Обрізання значень масиву за допомогою **trim()****

```php
<?php
function trim_value(&$value)
{
    $value = trim($value);
}

$fruit = array('apple','banana ', ' cranberry ');
var_dump($fruit);

array_walk($fruit, 'trim_value');
var_dump($fruit);

?>
```

Результат виконання цього прикладу:

```
array(3) {
  [0]=>
  string(5) "apple"
  [1]=>
  string(7) "banana "
  [2]=>
  string(11) " cranberry "
}
array(3) {
  [0]=>
  string(5) "apple"
  [1]=>
  string(6) "banana"
  [2]=>
  string(9) "cranberry"
}
```

### Примітки

> **Зауваження** **Можливі трюки: видалення символів із середини рядка**
> 
> Так як **trim()** видаляє символи з початку і кінця рядка string, то видалення (або не видалення) символів з середини рядка може здивувати . `trim('abc', 'bad')` видалить як 'a', так і 'b', тому що видалення 'a' зрушить 'b' до початку рядка, що також дозволить її видалити. Ось чому це "працює", тоді як `trim('abc', 'b')` очевидно ні.

### Дивіться також

-   [ltrim()](function.ltrim.md) - Видаляє пробіли (або інші символи) з початку рядка
-   [rtrim()](function.rtrim.md) - Видаляє прогалини (або інші символи) з кінця рядка
-   [strreplace()](function.str-replace.md) - Замінює всі входження рядка пошуку на рядок заміни

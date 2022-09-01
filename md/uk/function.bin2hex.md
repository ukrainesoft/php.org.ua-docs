---
navigation:
  - function.addslashes.md: « addslashes
  - function.chop.md: chop »
  - index.md: PHP Manual
  - ref.strings.md: Функції для роботи з рядками
title: bin2hex
---
# bin2hex

(PHP 4, PHP 5, PHP 7, PHP 8)

bin2hex - Перетворює бінарні дані в шістнадцяткове уявлення

### Опис

```methodsynopsis
bin2hex(string $string): string
```

Повертає ASCII-рядок, що містить шістнадцяткове подання аргументу `string`. Перетворення провадиться побайтно, починаючи з верхнього напівбайта.

### Список параметрів

`string`

Рядок.

### Значення, що повертаються

Повертає шістнадцяткове подання зазначеного рядка.

### Приклади

**Приклад #1 Приклад використання **bin2hex()****

```php
<?php

$hex = bin2hex('Hello world!');

var_dump($hex);
var_dump(hex2bin($hex));
?>
```

Результат виконання цього прикладу:

```
string(24) "48656c6c6f20776f726c6421"
string(12) "Hello world!"
```

### Дивіться також

-   [hex2bin()](function.hex2bin.md) - Перетворює шістнадцяткові дані на двійкові
-   [pack()](function.pack.md) - Упакувати дані у бінарний рядок

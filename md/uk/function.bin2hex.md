---
navigation:
  - function.addslashes.md: « addslashes
  - function.chop.md: chop »
  - index.md: PHP Manual
  - ref.strings.md: Функції для роботи з рядками
title: bin2hex
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# bin2hex

(PHP 4, PHP 5, PHP 7, PHP 8)

bin2hex - Перетворює бінарні дані в шістнадцяткове уявлення

### Опис

```methodsynopsis
bin2hex(string $string): string
```

Возвращает ASCII-строку, содержащую шестнадцатеричное представление аргумента`string`Преобразование производится побайтно, начиная с верхнего полубайта.

### Список параметрів

`string`

Рядок.

### Значення, що повертаються

Повертає шістнадцяткове подання зазначеного рядка.

### Приклади

**Пример #1 Пример использования функции**bin2hex()\*\*\*\*

```php
<?php

$hex = bin2hex('Hello world!');

var_dump($hex);
var_dump(hex2bin($hex));
?>
```

Результат виконання наведеного прикладу:

```
string(24) "48656c6c6f20776f726c6421"
string(12) "Hello world!"
```

### Дивіться також

-   [hex2bin()](function.hex2bin.md) \- Перетворює шістнадцяткові дані на двійкові
-   [pack()](function.pack.md) \- Упакувати дані у бінарний рядок

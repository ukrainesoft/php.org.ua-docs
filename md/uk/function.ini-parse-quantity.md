---
navigation:
  - function.ini-get.md: « ini\_get
  - function.ini-restore.md: ini\_restore »
  - index.md: PHP Manual
  - ref.info.md: Опції PHP/інформаційні функції
title: ini\_parse\_quantity
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ini\_parse\_quantity

(PHP 8 >= 8.2.0)

ini\_parse\_quantity — Get interpreted size from ini shorthand syntax

### Опис

```methodsynopsis
ini_parse_quantity(string $shorthand): int
```

У разі успішного виконання повертає інтерпретований розмір у байтах з [скорочень байтових значень](faq.using.md#faq.using.shorthandbytes)

### Список параметрів

`shorthand`

Скорочення байтових значень для розбору, має бути числом, за яким слідує необов'язковий множник. Підтримуються такі множники: `k` `K` `1024` `m` `M` `1048576` `g` `G` `1073741824`). Число може бути десятковим, шістнадцятковим (з префіксом `0x`или`0X`), вісімковим (з префіксом `0o` `0O`или ) або двійковим (з префіксом `0b`или`0B`

### Значення, що повертаються

Повертає інтерпретований розмір у байтах у вигляді цілого числа (int).

### Помилки

Якщо значення не може бути розібране або використовується неприпустимий множник, видається помилка рівня **`E_WARNING`**

### Приклади

**Приклад #1 Приклад використання** ini\_parse\_quantity()\*\*\*\*

```php
<?php

var_dump(ini_parse_quantity('1024'));
var_dump(ini_parse_quantity('1024M'));
var_dump(ini_parse_quantity('512K'));
var_dump(ini_parse_quantity('0xFFk'));
var_dump(ini_parse_quantity('0b1010k'));
var_dump(ini_parse_quantity('0o1024'));
var_dump(ini_parse_quantity('01024'));
var_dump(ini_parse_quantity('Foobar'));
var_dump(ini_parse_quantity('10F'));

?>
```

Висновок наведеного прикладу буде схожим на:

```
int(1024)
int(1073741824)
int(524288)
int(261120)
int(10240)
int(532)
int(532)

Warning: Invalid quantity "Foobar": no valid leading digits, interpreting as "0" for backwards compatibility
int(0)

Warning: Invalid quantity "10F": unknown multiplier "F", interpreting as "10" for backwards compatibility
int(10)
```

### Дивіться також

-   [ini\_get()](function.ini-get.md) \- Отримує значення налаштування конфігурації

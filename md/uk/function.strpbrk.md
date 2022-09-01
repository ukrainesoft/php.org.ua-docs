---
navigation:
  - function.strncmp.html: « strncmp
  - function.strpos.html: strpos »
  - index.html: PHP Manual
  - ref.strings.html: Функції для роботи з рядками
title: strpbrk
---
# strpbrk

(PHP 5, PHP 7, PHP 8)

strpbrk — Шукає у рядку будь-який символ із заданого набору

### Опис

```methodsynopsis
strpbrk(string $string, string $characters): string|false
```

**strpbrk()** шукає у рядку `string` символи з набору `characters`

### Список параметрів

`string`

Рядок, в якому проводиться пошук `characters`

`characters`

Цей параметр чутливий до регістру.

### Значення, що повертаються

Повертає рядок, починаючи зі знайденого символу, або \*\*`false`\*\*якщо він не був знайдений.

### Приклади

**Приклад #1 Приклад використання **strpbrk()****

```php
<?php

$text = 'This is a Simple text.';

// Этот код выдаст "is is a Simple text.", т.к. символ 'i' встретится раньше
echo strpbrk($text, 'mi');

// Этот код выдаст "Simple text.", т.к. символы чувствительны к регистру
echo strpbrk($text, 'S');
?>
```

### Дивіться також

-   [strpos()](function.strpos.html) - Повертає позицію першого входження підрядка
-   [strstr()](function.strstr.html) - Знаходить перше входження підрядка
-   [pregmatch()](function.preg-match.html) - Виконує перевірку на відповідність регулярному виразу

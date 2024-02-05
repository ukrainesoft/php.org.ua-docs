---
navigation:
  - function.strncmp.md: « strncmp
  - function.strpos.md: strpos »
  - index.md: PHP Manual
  - ref.strings.md: Функції для роботи з рядками
title: strpbrk
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
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

**Пример #1 Пример использования**strpbrk()\*\*\*\*

```php
<?php

$text = 'This is a Simple text.';

// Этот код выдаст "is is a Simple text.", т.к. символ 'i' встретится раньше
echo strpbrk($text, 'mi');

// Этот код выдаст "Simple text.", т.к. символы чувствительны к регистру
echo strpbrk($text, 'S');
?>
```

### Дивіться також

-   [strpos()](function.strpos.md) \- Повертає позицію першого входження підрядка
-   [strstr()](function.strstr.md) \- Знаходить перше входження підрядка
-   [preg\_match()](function.preg-match.md) \- Виконує перевірку на відповідність регулярному виразу

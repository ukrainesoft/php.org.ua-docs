---
navigation:
  - function.ob-get-flush.md: « ob\_get\_flush
  - function.ob-get-level.md: ob\_get\_level »
  - index.md: PHP Manual
  - ref.outcontrol.md: Функції контролю виведення
title: ob\_get\_length
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ob\_get\_length

(PHP 4 >= 4.0.2, PHP 5, PHP 7, PHP 8)

ob\_get\_length — Повертає розмір буфера виводу

### Опис

```methodsynopsis
ob_get_length(): int|false
```

Поверне розмір у байтах вмісту у буфері виводу.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає розмір у байтах вмісту буфера виводу або \*\*`false`\*\*якщо буферизація не активна.

### Приклади

**Приклад #1 Простий приклад використання функції **ob\_get\_length()****

```php
<?php

ob_start();

echo "Привет ";

$len1 = ob_get_length();

echo "Мир";

$len2 = ob_get_length();

ob_end_clean();

echo $len1 . ", " . $len2;
?>
```

Результат виконання наведеного прикладу:

```
13, 19
```

### Дивіться також

-   [ob\_start()](function.ob-start.md) \- Включає буферизацію виводу
-   [ob\_get\_contents()](function.ob-get-contents.md) \- Повертає вміст буфера виводу

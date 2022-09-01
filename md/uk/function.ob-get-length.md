---
navigation:
  - function.ob-get-flush.html: « obgetflush
  - function.ob-get-level.html: проgetlevel »
  - index.md: PHP Manual
  - ref.outcontrol.md: Функції контролю виведення
title: проgetlength
---
# проgetlength

(PHP 4> = 4.0.2, PHP 5, PHP 7, PHP 8)

проgetlength — Повертає розмір буфера виводу

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

**Приклад #1 Простий приклад використання функції **проgetlength()****

```php
<?php

ob_start();

echo "Привет ";

$len1 = ob_get_length();

echo "Мир";

$len2 = ob_get_length();

ob_end_clean();

echo $len1 . ", " . $len2;
?>
```

Результат виконання цього прикладу:

```
13, 19
```

### Дивіться також

-   [проstart()](function.ob-start.html) - Включення буферизації виводу
-   [проgetcontents()](function.ob-get-contents.html) - Повертає вміст буфера виводу

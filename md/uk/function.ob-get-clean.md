---
navigation:
  - function.ob-flush.md: « obflush
  - function.ob-get-contents.md: проgetcontents »
  - index.md: PHP Manual
  - ref.outcontrol.md: Функції контролю виведення
title: проgetclean
---
# проgetclean

(PHP 4> = 4.3.0, PHP 5, PHP 7, PHP 8)

проgetclean — Отримати вміст поточного буфера та видалити його.

### Опис

```methodsynopsis
ob_get_clean(): string|false
```

Отримує вміст поточного буфера, а потім видаляє поточний буфер.

**проgetclean()** по суті виконує [проgetcontents()](function.ob-get-contents.md) і [проendclean()](function.ob-end-clean.md)

Буфер виводу має запускатися функцією [проstart()](function.ob-start.md) з прапорами [PHPOUTPUTHANDLERCLEANABLE](outcontrol.constants.md#constant.php-output-handler-cleanable) і [PHPOUTPUTHANDLERREMOVABLE](outcontrol.constants.md#constant.php-output-handler-removable). Інакше **проgetclean()** не спрацює.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає вміст буфера виводу та закінчує буферизацію виводу. Якщо буферизація виводу не активована, то функція поверне **`false`**

### Приклади

**Приклад #1 Простий приклад використання функції **проgetclean()****

```php
<?php

ob_start();

echo "Привет мир";

$out = ob_get_clean();
$out = strtolower($out);

var_dump($out);
?>
```

Результат виконання цього прикладу:

```
string(11) "привет мир"
```

### Дивіться також

-   [проgetcontents()](function.ob-get-contents.md) - Повертає вміст буфера виводу
-   [проstart()](function.ob-start.md) - Включення буферизації виводу

---
navigation:
  - function.ob-get-clean.md: « obgetclean
  - function.ob-get-flush.md: проgetflush »
  - index.md: PHP Manual
  - ref.outcontrol.md: Функції контролю виведення
title: проgetcontents
---
# проgetcontents

(PHP 4, PHP 5, PHP 7, PHP 8)

проgetcontents — Повертає вміст буфера виводу

### Опис

```methodsynopsis
ob_get_contents(): string|false
```

Отримує вміст буфера без його очищення.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція поверне вміст буфера виводу або **`false`**, якщо буферизація виводу не активована.

### Приклади

**Приклад #1 Простий приклад використання функції **проgetcontents()****

```php
<?php

ob_start();

echo "Привет ";

$out1 = ob_get_contents();

echo "Мир";

$out2 = ob_get_contents();

ob_end_clean();

var_dump($out1, $out2);
?>
```

Результат виконання цього прикладу:

```
string(6) "Привет "
string(11) "Привет Мир"
```

### Дивіться також

-   [проstart()](function.ob-start.md) - Включення буферизації виводу
-   [проgetlength()](function.ob-get-length.md) - Повертає розмір буфера виводу

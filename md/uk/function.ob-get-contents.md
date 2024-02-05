---
navigation:
  - function.ob-get-clean.md: « ob\_get\_clean
  - function.ob-get-flush.md: ob\_get\_flush »
  - index.md: PHP Manual
  - ref.outcontrol.md: Функції контролю виведення
title: ob\_get\_contents
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ob\_get\_contents

(PHP 4, PHP 5, PHP 7, PHP 8)

ob\_get\_contents — Повертає вміст буфера виводу

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

**Приклад #1 Простий приклад використання функції **ob\_get\_contents()****

```php
<?php

ob_start();

echo "Привет ";

$out1 = ob_get_contents();

echo "Мир";

$out2 = ob_get_contents();

ob_end_clean();

var_dump($out1, $out2);
?>
```

Результат виконання наведеного прикладу:

```
string(6) "Привет "
string(11) "Привет Мир"
```

### Дивіться також

-   [ob\_start()](function.ob-start.md) \- Включає буферизацію виводу
-   [ob\_get\_length()](function.ob-get-length.md) \- Повертає розмір буфера виводу

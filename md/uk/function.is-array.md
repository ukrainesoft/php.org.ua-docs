---
navigation:
  - function.intval.md: « intval
  - function.is-bool.html: ісbool »
  - index.md: PHP Manual
  - ref.var.md: Функції для роботи зі змінними
title: ісarray
---
# ісarray

(PHP 4, PHP 5, PHP 7, PHP 8)

ісarray - Визначає, чи є змінна масивом

### Опис

```methodsynopsis
is_array(mixed $value): bool
```

Визначає, чи є змінна масивом.

### Список параметрів

`value`

Перевірена змінна.

### Значення, що повертаються

Повертає **`true`**, якщо змінна `value` є масивом (array), або **`false`** в іншому випадку.

### Приклади

**Приклад #1 Перевіряє, чи є змінна масивом**

```php
<?php
$yes = array('это', 'Масив');

echo is_array($yes) ? 'Масив' : 'Не Масив';
echo "\n";

$no = 'это строка';

echo is_array($no) ? 'Масив' : 'Не Масив';
?>
```

Результат виконання цього прикладу:

```
Масив
Не Масив
```

### Дивіться також

-   [ісfloat()](function.is-float.html) - Перевіряє, чи є змінна числом із плаваючою точкою
-   [ісint()](function.is-int.html) - Перевіряє, чи є змінна цілим числом
-   [ісstring()](function.is-string.html) - Перевіряє, чи є змінним рядком
-   [ісobject()](function.is-object.html) - Перевіряє, чи є змінна об'єктом

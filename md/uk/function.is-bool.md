---
navigation:
  - function.is-array.md: « is\_array
  - function.is-callable.md: is\_callable »
  - index.md: PHP Manual
  - ref.var.md: Функції для роботи зі змінними
title: is\_bool
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# is\_bool

(PHP 4, PHP 5, PHP 7, PHP 8)

is\_bool — Перевіряє, чи є змінна логічне значення

### Опис

```methodsynopsis
is_bool(mixed $value): bool
```

Перевіряє, чи є змінна логічне значення.

### Список параметрів

`value`

Перевірена змінна.

### Значення, що повертаються

Повертає **`true`**, если значение`value` - Логічне (bool), інакше **`false`**

### Приклади

**Приклад #1 Приклад использования функции**is\_bool()\*\*\*\*

```php
<?php

$a = false;
$b = 0;

// Поскольку переменная $a — логическая переменная, функция вернёт true
if (is_bool($a) === true) {
    echo "Да, это логическая переменная";
}

// Поскольку переменная $b — не логическая переменная, функция вернёт false
if (is_bool($b) === false) {
    echo "Нет, это не логическая переменная";
}

?>
```

### Дивіться також

-   [is\_float()](function.is-float.md) \- Перевіряє, чи є змінна число з плаваючою точкою
-   [is\_int()](function.is-int.md) \- Перевіряє, чи є змінна ціла кількість
-   [is\_string()](function.is-string.md) \- Перевіряє, чи є тип змінної рядок
-   [is\_object()](function.is-object.md) \- Перевіряє, чи є змінна об'єкт
-   [is\_array()](function.is-array.md) \- Визначає, чи є змінна масив

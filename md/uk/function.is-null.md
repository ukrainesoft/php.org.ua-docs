---
navigation:
  - function.is-long.md: « is\_long
  - function.is-numeric.md: is\_numeric »
  - index.md: PHP Manual
  - ref.var.md: Функції для роботи зі змінними
title: is\_null
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# is\_null

(PHP 4 >= 4.0.4, PHP 5, PHP 7, PHP 8)

is\_null — Перевіряє, чи значення змінної дорівнює **`null`**

### Опис

```methodsynopsis
is_null(mixed $value): bool
```

Перевіряє, чи значення змінної **`null`**

### Список параметрів

`value`

Перевірена змінна.

### Значення, що повертаються

Повертає **`true`**, если значение`value`— null, иначе\*\*`false`\*\*

### Приклади

**Пример #1 Пример использования функции**is\_null()\*\*\*\*

```php
<?php

error_reporting(E_ALL);

$foo = NULL;
var_dump(is_null($inexistent), is_null($foo));

?>
```

```
Notice: Undefined variable: inexistent in ...
bool(true)
bool(true)
```

### Дивіться також

-   Тип[**`null`**](language.types.null.md#language.types.null.syntax)
-   [isset()](function.isset.md) \- Визначає, чи була встановлена ​​змінна значенням, відмінним від null
-   [is\_bool()](function.is-bool.md) \- Перевіряє, чи є змінна логічне значення
-   [is\_numeric()](function.is-numeric.md) \- Перевіряє, чи містить змінне число чи числове рядок
-   [is\_float()](function.is-float.md) \- Перевіряє, чи є змінна число з плаваючою точкою
-   [is\_int()](function.is-int.md) \- Перевіряє, чи є змінна ціла кількість
-   [is\_string()](function.is-string.md) \- Перевіряє, чи є тип змінної рядок
-   [is\_object()](function.is-object.md) \- Перевіряє, чи є змінна об'єкт
-   [is\_array()](function.is-array.md) \- Визначає, чи є змінна масив

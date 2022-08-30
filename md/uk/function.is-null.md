Перевіряє, чи значення змінної дорівнює null

-   [« islong](function.is-long.html)
    
-   [ісnumeric »](function.is-numeric.html)
    
-   [PHP Manual](index.html)
    
-   [Функції для роботи зі змінними](ref.var.html)
    
-   Перевіряє, чи значення змінної дорівнює null
    

# ісnull

(PHP 4> = 4.0.4, PHP 5, PHP 7, PHP 8)

ісnull — Перевіряє, чи значення змінної дорівнює **`null`**

### Опис

```methodsynopsis
is_null(mixed $value): bool
```

Перевіряє, чи значення цієї змінної дорівнює **`null`**

### Список параметрів

`value`

Перевірена змінна.

### Значення, що повертаються

Повертає **`true`**, якщо значення `value` одно null, або **`false`** в іншому випадку.

### Приклади

**Приклад #1 Приклад використання **ісnull()****

```php
<?php

error_reporting(E_ALL);

$foo = NULL;
var_dump(is_null($inexistent), is_null($foo));

?>
```

```
Notice: Undefined variable: inexistent in ...
bool(true)
bool(true)
```

### Дивіться також

-   Тип [**`null`**](language.types.null.html#language.types.null.syntax)
-   [isset()](function.isset.html) - Визначає, чи була встановлена ​​змінна значенням, відмінним від null
-   [ісbool()](function.is-bool.html) - Перевіряє, чи є змінна булевою
-   [ісnumeric()](function.is-numeric.html) - Перевіряє, чи є змінна числом чи рядком, що містить число
-   [ісfloat()](function.is-float.html) - Перевіряє, чи є змінна числом із плаваючою точкою
-   [ісint()](function.is-int.html) - Перевіряє, чи є змінна цілим числом
-   [ісstring()](function.is-string.html) - Перевіряє, чи є змінним рядком
-   [ісobject()](function.is-object.html) - Перевіряє, чи є змінна об'єктом
-   [ісarray()](function.is-array.html) - Визначає, чи є змінна масивом
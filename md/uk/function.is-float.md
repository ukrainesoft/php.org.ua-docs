Перевіряє, чи є змінна числом з плаваючою точкою

-   [« is\_double](function.is-double.html)
    
-   [is\_int »](function.is-int.html)
    
-   [PHP Manual](index.html)
    
-   [Функции для работы с переменными](ref.var.html)
    
-   Перевіряє, чи є змінна числом з плаваючою точкою
    

# ісfloat

(PHP 4, PHP 5, PHP 7, PHP 8)

ісfloat — Перевіряє, чи є змінна числом із плаваючою точкою

### Опис

```methodsynopsis
is_float(mixed $value): bool
```

Перевіряє, чи є змінна числом з плаваючою точкою.

> **Зауваження**
> 
> Щоб перевірити, чи є змінна числом або рядком, що містить число (як поле введення у формі, яке завжди є рядком), використовуйте [is\_numeric()](function.is-numeric.html)

### Список параметрів

`value`

Перевірена змінна.

### Значення, що повертаються

Повертає **`true`**, якщо `value` є змінною типу float, **`false`** в іншому випадку.

### Приклади

**Приклад #1 Приклад використання **ісfloat()****

```php
var_dump(is_float(27.25));
var_dump(is_float('abc'));
var_dump(is_float(23));
var_dump(is_float(23.5));
var_dump(is_float(1e7));  //Научная нотация
var_dump(is_float(true));
?>
```

Результат виконання цього прикладу:

```
bool(true)
bool(false)
bool(false)
bool(true)
bool(true)
bool(false)
```

### Дивіться також

-   [is\_bool()](function.is-bool.html) - Перевіряє, чи є змінна булевою
-   [is\_int()](function.is-int.html) - Перевіряє, чи є змінна цілим числом
-   [is\_numeric()](function.is-numeric.html) - Перевіряє, чи є змінна числом або рядком, що містить число
-   [is\_string()](function.is-string.html) - Перевіряє, чи є змінним рядком
-   [is\_array()](function.is-array.html) - Визначає, чи є змінна масивом
-   [is\_object()](function.is-object.html) - Перевіряє, чи є змінна об'єктом
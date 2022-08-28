Перевіряє, чи є змінна булевою

-   [« is\_array](function.is-array.html)
    
-   [is\_callable »](function.is-callable.html)
    
-   [PHP Manual](index.html)
    
-   [Функции для работы с переменными](ref.var.html)
    
-   Перевіряє, чи є змінна булевою
    

# ісbool

(PHP 4, PHP 5, PHP 7, PHP 8)

ісbool — Перевіряє, чи є змінна булевою

### Опис

```methodsynopsis
is_bool(mixed $value): bool
```

Перевіряє, чи є ця змінна булевою.

### Список параметрів

`value`

Перевірена змінна.

### Значення, що повертаються

Повертає **`true`**, якщо `value` є змінною типу bool, або **`false`** в іншому випадку.

### Приклади

**Приклад #1 Приклад використання **ісbool()****

```php
<?php
$a = false;
$b = 0;

// Так как $a является булевой переменной, функция вернёт true
if (is_bool($a) === true) {
    echo "Да, это булевая переменная";
}

// Так как $b не является булевой переменной, функция вернёт false
if (is_bool($b) === false) {
    echo "Нет, это не булевая переменная";
}
?>
```

### Дивіться також

-   [is\_float()](function.is-float.html) - Перевіряє, чи є змінна числом із плаваючою точкою
-   [is\_int()](function.is-int.html) - Перевіряє, чи є змінна цілим числом
-   [is\_string()](function.is-string.html) - Перевіряє, чи є змінним рядком
-   [is\_object()](function.is-object.html) - Перевіряє, чи є змінна об'єктом
-   [is\_array()](function.is-array.html) - Визначає, чи є змінна масивом
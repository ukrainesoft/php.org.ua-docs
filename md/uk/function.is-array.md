Визначає, чи є змінна масивом

-   [« intval](function.intval.html)
    
-   [is\_bool »](function.is-bool.html)
    
-   [PHP Manual](index.html)
    
-   [Функции для работы с переменными](ref.var.html)
    
-   Визначає, чи є змінна масивом
    

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
$yes = array('это', 'массив');

echo is_array($yes) ? 'Массив' : 'Не массив';
echo "\n";

$no = 'это строка';

echo is_array($no) ? 'Массив' : 'Не массив';
?>
```

Результат виконання цього прикладу:

```
Массив
Не массив
```

### Дивіться також

-   [is\_float()](function.is-float.html) - Перевіряє, чи є змінна числом із плаваючою точкою
-   [is\_int()](function.is-int.html) - Перевіряє, чи є змінна цілим числом
-   [is\_string()](function.is-string.html) - Перевіряє, чи є змінним рядком
-   [is\_object()](function.is-object.html) - Перевіряє, чи є змінна об'єктом
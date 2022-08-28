Повертає кодування поточного з'єднання CUBRID

-   [« cubrid\_get\_autocommit](function.cubrid-get-autocommit.html)
    
-   [cubrid\_get\_class\_name »](function.cubrid-get-class-name.html)
    
-   [PHP Manual](index.html)
    
-   [Функции CUBRID](ref.cubrid.html)
    
-   Повертає кодування поточного з'єднання CUBRID
    

# cubridgetcharset

(PECL CUBRID >= 8.3.0)

cubridgetcharset — Повертає кодування поточного з'єднання CUBRID

### Опис

```methodsynopsis
cubrid_get_charset(resource $conn_identifier): string
```

Ця функція повертає кодування поточного з'єднання CUBRID та аналогічна функції сумісності CUBRID MySQL [cubrid\_client\_encoding()](function.cubrid-client-encoding.html)

### Список параметрів

`conn_identifier`

Ідентифікатор з'єднання.

### Значення, що повертаються

Рядок, що містить кодування поточного з'єднання CUBRID у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **cubridgetcharset()****

```php
<?php

$con = cubrid_connect("localhost", 33000, "demodb");
if (!$con)
{
    die('Could not connect.');
}

printf("CUBRID current charset: %s\n", cubrid_get_charset($con));

?>
```

Результат виконання цього прикладу:

```
CUBRID current charset: iso8859-1
```

### Дивіться також

-   [cubrid\_client\_encoding()](function.cubrid-client-encoding.html) - Повертає кодування поточного з'єднання CUBRID
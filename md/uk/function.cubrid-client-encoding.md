Повертає кодування поточного з'єднання CUBRID

-   [« cubrid\_affected\_rows](function.cubrid-affected-rows.html)
    
-   [cubrid\_close »](function.cubrid-close.html)
    
-   [PHP Manual](index.html)
    
-   [Функции совместимости CUBRID MySQL](cubridmysql.cubrid.html)
    
-   Повертає кодування поточного з'єднання CUBRID
    

# cubridclientencoding

(PECL CUBRID >= 8.3.1)

cubridclientencoding — Повертає кодування поточного з'єднання CUBRID

### Опис

```methodsynopsis
cubrid_client_encoding(resource $conn_identifier = ?): string
```

Функція повертає кодування поточного з'єднання CUBRID та аналогічна функції **cubridgetencoding()**

### Список параметрів

`conn_identifier`

Ідентифікатор з'єднання. Якщо не встановлено, то буде використано останнє відкрите за допомогою [cubrid\_connect()](function.cubrid-connect.html) з'єднання.

### Значення, що повертаються

Рядок, що містить кодування поточного з'єднання CUBRID у разі успішного виконання.

**`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **cubridclientencoding()****

```php
<?php

$con = cubrid_connect("localhost", 33000, "demodb");
if (!$con)
{
    die('Не получилось подключиться.');
}

printf("Текущая кодировка CUBRID: %s\n", cubrid_client_encoding($con));

?>
```

Результат виконання цього прикладу:

```
Текущая кодировка CUBRID: iso8859-1
```

### Дивіться також

-   [cubrid\_get\_charset()](function.cubrid-get-charset.html) - Повертає кодування поточного з'єднання CUBRID
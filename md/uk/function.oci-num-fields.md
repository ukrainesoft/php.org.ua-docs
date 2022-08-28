Повертає кількість полів у результаті запиту

-   [« oci\_new\_descriptor](function.oci-new-descriptor.html)
    
-   [oci\_num\_rows »](function.oci-num-rows.html)
    
-   [PHP Manual](index.html)
    
-   [OCI8 Функции](ref.oci8.html)
    
-   Повертає кількість полів у результаті запиту
    

# ocinumfields

(PHP 5, PHP 7, PHP 8, PECL OCI8> = 1.1.0)

ocinumfields — Повертає кількість полів через запит

### Опис

```methodsynopsis
oci_num_fields(resource $statement): int
```

Отримує кількість стовпців у запиті, заданому в `statement`

### Список параметрів

`statement`

Ідентифікатор допустимого запиту OCI.

### Значення, що повертаються

Повертає кількість порушених рядків у вигляді цілого числа (int).

### Приклади

**Приклад #1 Приклад використання **ocinumfields()****

```php
<?php

// Создате таблицу:
//   CREATE TABLE mytab (id NUMBER, quantity NUMBER);

$conn = oci_connect("hr", "hrpwd", "localhost/XE");
if (!$conn) {
    $m = oci_error();
    trigger_error(htmlentities($m['message']), E_USER_ERROR);
}

$stid = oci_parse($conn, "SELECT * FROM mytab");
oci_execute($stid, OCI_DESCRIBE_ONLY); // используйте OCI_DESCRIBE_ONLY, если не получаете данных

$ncols = oci_num_fields($stid);
for ($i = 1; $i <= $ncols; $i++) {
    echo oci_field_name($stid, $i) . " " . oci_field_type($stid, $i) . "<br>\n";
}

// Выведет:
//    ID NUMBER
//    QUANTITY NUMBER

oci_free_statement($stid);
oci_close($conn);

?>
```

### Примітки

> **Зауваження**
> 
> У версіях PHP нижче 5.0.0 ця функція називалася [ocinumcols()](function.ocinumcols.html). У PHP 5.0.0 і вище [ocinumcols()](function.ocinumcols.html) є аліасом **ocinumfields()**Тому ви можете продовжувати використовувати це ім'я, однак це не рекомендується.
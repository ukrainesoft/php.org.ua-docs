Перевіряє, чи дорівнює поле в поточному отриманому ряду null

-   [« ocifetch](function.oci-fetch.html)
    
-   [ocifieldname »](function.oci-field-name.html)
    
-   [PHP Manual](index.html)
    
-   [OCI8 Функции](ref.oci8.html)
    
-   Перевіряє, чи дорівнює поле в поточному отриманому ряду null
    

# ocifieldісnull

(PHP 5, PHP 7, PHP 8, PECL OCI8> = 1.1.0)

ocifieldісnull — Перевіряє, чи рівне поле в поточному отриманому ряду рівним **`null`**

### Опис

```methodsynopsis
oci_field_is_null(resource $statement, string|int $column): bool
```

Перевіряє, чи є значення, передане в поле `column` з поточного ряду `statement` рівним **`null`**

### Список параметрів

`statement`

Ідентифікатор допустимого запиту OCI.

`column`

Може бути порядковий номер поля (з 1) або ім'я поля.

### Значення, що повертаються

Повертає **`true`**, якщо `column` дорівнює **`null`**, і **`false`** якщо ні.

### Приклади

**Приклад #1 Приклад використання [ocifieldname()](function.oci-field-name.html)**

```php
<?php

// Создайте таблицу:
//   CREATE TABLE mytab (c1 NUMBER);
//   INSERT INTO mytab VALUES (1);
//   INSERT INTO mytab VALUES (NULL);

$conn = oci_connect("hr", "hrpwd", "localhost/XE");
if (!$conn) {
    $m = oci_error();
    trigger_error(htmlentities($m['message']), E_USER_ERROR);
}

$stid = oci_parse($conn, "SELECT * FROM mytab");
oci_execute($stid);

while (($row = oci_fetch_array($stid, OCI_RETURN_NULLS)) != false) {
    $ncols = oci_num_fields($stid);
    for ($col = 1; $col <= $ncols; $col++) {
        var_dump(oci_field_is_null($stid, $col));
    }
}

// Выведет:
//    bool(false)
//    bool(true)

oci_free_statement($stid);
oci_close($conn);

?>
```

### Примітки

> **Зауваження**
> 
> У версіях PHP нижче 5.0.0 ця функція називалася [ocicolumnisnull()](function.ocicolumnisnull.html). У PHP 5.0.0 і вище [ocicolumnisnull()](function.ocicolumnisnull.html) є аліасом \*\*ocifieldісnull()\*\*Тому ви можете продовжувати використовувати це ім'я, однак це не рекомендується.
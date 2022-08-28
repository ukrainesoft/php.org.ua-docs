Повертає ідентифікатор створеного курсору

-   [« oci\_new\_connect](function.oci-new-connect.html)
    
-   [oci\_new\_descriptor »](function.oci-new-descriptor.html)
    
-   [PHP Manual](index.html)
    
-   [OCI8 Функции](ref.oci8.html)
    
-   Повертає ідентифікатор створеного курсору
    

# ocinewcursor

(PHP 5, PHP 7, PHP 8, PECL OCI8> = 1.1.0)

ocinewcursor — Повертає ідентифікатор створеного курсору

### Опис

```methodsynopsis
oci_new_cursor(resource $connection): resource|false
```

Створює новий курсор для зазначеного з'єднання та повертає його ідентифікатор.

### Список параметрів

`connection`

Ідентифікатор з'єднання з сервером Oracle, який повертається функцією [oci\_connect()](function.oci-connect.html) або [oci\_pconnect()](function.oci-pconnect.html)

### Значення, що повертаються

Повертає покажчик на новий вираз або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Прив'язка REF CURSOR у виклику процедур, що зберігаються Oracle**

```php
<?php

// Предварительная подготовка:
//   создайте или замените процедуру myproc(myrc out sys_refcursor) как
//   begin
//     open myrc for select first_name from employees;
//   end;

$conn = oci_connect("hr", "hrpwd", "localhost/XE");
if (!$conn) {
    $m = oci_error();
    trigger_error(htmlentities($m['message']), E_USER_ERROR);
}

$curs = oci_new_cursor($conn);
$stid = oci_parse($conn, "begin myproc(:cursbv); end;");
oci_bind_by_name($stid, ":cursbv", $curs, -1, OCI_B_CURSOR);
oci_execute($stid);

oci_execute($curs);  // Выполняет REF CURSOR как обычный идентификатор выражения
while (($row = oci_fetch_array($curs, OCI_ASSOC+OCI_RETURN_NULLS)) != false) {
    echo $row['FIRST_NAME'] . "<br />\n";
}

oci_free_statement($stid);
oci_free_statement($curs);
oci_close($conn);

?>
```

### Примітки

> **Зауваження**
> 
> У версіях PHP нижче 5.0.0 ця функція називалася [ocinewcursor()](function.ocinewcursor.html). У PHP 5.0.0 і вище [ocinewcursor()](function.ocinewcursor.html) є аліасом **ocinewcursor()**Тому ви можете продовжувати використовувати це ім'я, однак це не рекомендується.